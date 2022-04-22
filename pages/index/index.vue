<template>
	<div id="mars2dContainer" class="mars2d-container"></div>
</template>

<script>
	import "leaflet/dist/leaflet.css"
	import L from "leaflet"

	import "mars2d/dist/mars2d.css"
	import * as mars2d from 'mars2d'
	import 'mars2d-esri'

	export default {
		data() {
			return {
				title: 'mars2d'
			}
		},
		mounted() {
			var mapOptions = {
				"zoom": 13,
				"center": { "lng": 117.240601, "lat": 31.827107 },
				"minZoom": 2,
				"maxZoom": 18,
				"centerAutoLevel": 15,
				"control": {
				  "scale": true,
				  "locationBar": {
					"crs": "CGCS2000_GK_Zone_3",
					"template": "<div>经度:{lng}</div> <div>纬度:{lat}</div> <div class='hide700'>横{crsx}  纵{crsy}</div> <div>层级:{level}</div>"
				  },
				  "layers": { "position": "topleft" },
				  "zoom": { "position": "bottomleft" },
				  "toolBar": { "position": "bottomleft" }
				},    
				"basemaps": [
				  {
					"pid": 10,
					"name": "天地图电子",
					"icon": "img/basemaps/tianditumap.png",
					"type": "group",
					"layers": [
					  {
						"name": "底图",
						"type": "tdt",
						"layer": "vec_d",
						"key": ["bcc62222fc634ec736589c483de933e6"]
					  },
					  {
						"name": "注记",
						"type": "tdt",
						"layer": "vec_z",
						"key": ["bcc62222fc634ec736589c483de933e6"]
					  }
					],
					"show": true
				  },
				  {
					"pid": 10,
					"name": "天地图卫星",
					"icon": "img/basemaps/tiandituimage.png",
					"type": "group",
					"layers": [
					  {
						"name": "底图",
						"type": "tdt",
						"layer": "img_d",
						"key": ["bcc62222fc634ec736589c483de933e6"]
					  },
					  {
						"name": "注记",
						"type": "tdt",
						"layer": "img_z",
						"key": ["bcc62222fc634ec736589c483de933e6"]
					  }
					]
				  },
				  {
					"pid": 10,
					"name": "OSM地图",
					"type": "xyz",
					"url": "http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
					"subdomains": "abc",
					"icon": "img/basemaps/bingmap.png"
				  },
				  {
					"id": 2021,
					"pid": 10,
					"name": "高德地图",
					"type": "gaode",
					"layer": "vec",
					"icon": "img/basemaps/bingmap.png"
				  },
				  {
					"pid": 10,
					"name": "高德卫星",
					"type": "group",
					"icon": "img/basemaps/googleimage.png",
					"layers": [
					  {
						"name": "底图",
						"type": "gaode",
						"layer": "img_d"
					  },
					  {
						"name": "注记",
						"type": "gaode",
						"layer": "img_z"
					  }
					]
				  },
				  {
					"pid": 10,
					"name": "mapbox深色",
					"type": "mapbox",
					"username": "marsgis",
					"styleId": "cki0a2mtc2vyo1bqu76p8ks8m",
					"icon": "img/basemaps/bd-c-light.png"
				  },
				  {
					"pid": 10,
					"name": "mapbox影像",
					"type": "mapbox",
					"username": "marsgis",
					"styleId": "cki0adkar2b0e19mv9tpiewld",
					"icon": "img/basemaps/bingimage.png"
				  },
				  {
					"pid": 10,
					"name": "灰色地图",
					"type": "arcgis",
					"url": "http://map.geoq.cn/ArcGIS/rest/services/ChinaOnlineStreetGray/MapServer",
					"chinaCRS": "GCJ02",
					"icon": "img/basemaps/bd-c-grayscale.png"
				  },
				  {
					"id": 2017,
					"pid": 10,
					"name": "蓝色地图",
					"type": "arcgis",
					"url": "http://map.geoq.cn/ArcGIS/rest/services/ChinaOnlineStreetPurplishBlue/MapServer",
					"chinaCRS": "GCJ02",
					"icon": "img/basemaps/bd-c-midnight.png"
				  }
				], 
			}
			var map = new mars2d.Map('mars2dContainer', mapOptions);

			console.log("map构造完成", map)
		},
		methods: {

		}
	}
</script>

<style>

</style>
