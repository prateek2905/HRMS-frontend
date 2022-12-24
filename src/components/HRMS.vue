<template>
    <div class="main">

    <div id="page-wrap">
        <div id="all">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Create offer letter section</a></li>
                <li><a href="#">Employee list</a></li>
                <li><a href="#">Company's information page</a></li>
            </ul>
        </div>
    </div>

    <div id="right-content">
        <div id="offer"><a href="#">Create Offer Letter</a></div>

        <div id="table">
            <table  >
                <thead>
                  <tr>
                    <th>Name</th>
                    <th>Compensation Awarded</th>
                    <th>Role Of Candidate</th>
                    <th>Offer Status</th>
                    <th>Offer Link</th>
                    <th>Career path</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="row in rows" :key="row.message">
                    <td><strong>{{row.name}}</strong></td>
                    <td>{{row.compensation}}</td>
                    <td>{{row.role}}</td>
                    <td>{{row.status}}</td>
                    <td>{{row.link}}</td>
                    <td>{{row.path}}</td>
                  </tr>
               </tbody>
              </table>
        </div>
    </div>

</div>
</template>

<script>
export default {
    name: "HRMS",
    data() {
        return {
            rows: [
                {
                    name: "Shubh",
                    compensation: "30000",
                    role: "Web dev",
                    status: "Pending",
                    link: "URL",
                    path: "...."
                },
                {
                    name: "Prateek",
                    compensation: "50000",
                    role: "SDE",
                    status: "Accepted",
                    link: "URL",
                    path: "...."
                },
                {
                    name: "Mohit",
                    compensation: "70000",
                    role: "SDE",
                    status: "Accepted",
                    link: "URL",
                    path: "...."
                }
            ]
        }
    }
}
</script>

<style>

body {
    background-color: #2c3e50;
}

.main{
    width: 80%;
    height: 80%;
    border-radius: 2%;
    display: flex;
    margin: auto;
    padding: 5%;
    flex-direction: row;
    justify-content: space-around;
}

#right-content{
	width: 80%;
}


#offer a{
    text-decoration: none;
    
    padding: 18px;
    background: #2c3e50;
    border-radius: 3px;
    color: #6b7278;
    text-align: center;
     
    font-family: 'Open Sans', sans-serif;
    font-weight: bold;
    font-size: 18px;
    font-variant: small-caps;
    font-weight: bold;
    -webkit-transition: all 0.2s ease;
    -moz-transition: all 0.2s ease;
    -o-transition: all 0.2s ease;
}

#all > ul {
    list-style: none;
    float: center;
    width: 200px;
    padding: 0 10px 0 0;
}

#all a {
    text-decoration: none;
    display: block;
    padding: 18px;
    background: #1d252c;
    border-radius: 3px;
    color: #6b7278;
    text-align: center;
    margin: 0 0 3px 0;
    font-family: 'Open Sans', sans-serif;
    font-weight: bold;
    font-size: 18px;
    font-variant: small-caps;
    font-weight: bold;
    -webkit-transition: all 0.2s ease;
    -moz-transition: all 0.2s ease;
    -o-transition: all 0.2s ease;
}

#all:hover a {
    opacity: 1.0;
}

#all:hover ul:hover a {
    opacity: 0.5;
}

#all:hover ul:hover a:hover {
    opacity: 1;
}

#all:active a {
    opacity: 1.0;
}

#all:active ul:active a {
    opacity: 0.5;
}

#all:active ul:active a:active {
    opacity: 0.9;
}

strong {
	font-weight: bold; 
}

em {
	font-style: italic; 
}

table {
	background: #f5f5f5;
	border-collapse: separate;
	box-shadow: inset 0 1px 0 #fff;
	font-size: 12px;
	line-height: 24px;
	margin: 0%;
	margin-top: 1.5rem;
	text-align: left;
	width: 90%;
}	

th {
	background: url(https://jackrugile.com/images/misc/noise-diagonal.png), linear-gradient(#777, #444);
	border-left: 1px solid #555;
	border-right: 1px solid #777;
	border-top: 1px solid #555;
	border-bottom: 1px solid #333;
	box-shadow: inset 0 1px 0 #999;
	color: #fff;
  font-weight: bold;
	padding: 10px 15px;
	position: relative;
	text-shadow: 0 1px 0 #000;	
}

th:after {
	background: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,.08));
	content: '';
	display: block;
	height: 25%;
	left: 0;
	margin: 1px 0 0 0;
	position: absolute;
	top: 25%;
	width: 100%;
}

th:first-child {
	border-left: 1px solid #777;	
	box-shadow: inset 1px 1px 0 #999;
}

th:last-child {
	box-shadow: inset -1px 1px 0 #999;
}

td {
	border-right: 1px solid #fff;
	border-left: 1px solid #e8e8e8;
	border-top: 1px solid #fff;
	border-bottom: 1px solid #e8e8e8;
	padding: 10px 15px;
	position: relative;
	transition: all 300ms;
}

td:first-child {
	box-shadow: inset 1px 0 0 #fff;
}	

td:last-child {
	border-right: 1px solid #e8e8e8;
	box-shadow: inset -1px 0 0 #fff;
}	

tr {
	background: url(https://jackrugile.com/images/misc/noise-diagonal.png);	
}

tr:nth-child(odd) td {
	background: #f1f1f1 url(https://jackrugile.com/images/misc/noise-diagonal.png);	
}

tr:last-of-type td {
	box-shadow: inset 0 -1px 0 #fff; 
}

tr:last-of-type td:first-child {
	box-shadow: inset 1px -1px 0 #fff;
}	

tr:last-of-type td:last-child {
	box-shadow: inset -1px -1px 0 #fff;
}	

tbody:hover td {
	color: transparent;
	text-shadow: 0 0 3px #aaa;
}

tbody:hover tr:hover td {
	color: #444;
	text-shadow: 0 1px 0 #fff;
}
</style>

