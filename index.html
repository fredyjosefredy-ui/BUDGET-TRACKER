<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Garcia Property Services Revenue Tracker</title>

<style>

body{
font-family:Arial, sans-serif;
margin:0;
background:#f3f6f4;
color:#222;
}

.container{
max-width:1200px;
margin:auto;
padding:20px;
}

h1{
text-align:center;
color:#02692a;
}

h2{
color:#02692a;
margin-bottom:5px;
}

.card{
background:white;
padding:15px;
border-radius:12px;
box-shadow:0 2px 6px rgba(0,0,0,.08);
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:12px;
margin-bottom:25px;
}

.card p{
font-size:20px;
font-weight:bold;
margin:0;
color:#02692a;
}

.form-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:10px;
margin-bottom:10px;
}

input,select,button{
padding:10px;
border-radius:8px;
border:1px solid #ccc;
font-size:14px;
}

button{
border:none;
cursor:pointer;
font-weight:bold;
}

.add{
background:#02692a;
color:white;
}

.delete{
background:#d33;
color:white;
padding:6px 10px;
}

.export{
background:#2563eb;
color:white;
}

.clear{
background:#b02a2a;
color:white;
}

table{
width:100%;
border-collapse:collapse;
margin-top:10px;
background:white;
}

th,td{
padding:10px;
border-bottom:1px solid #eee;
text-align:left;
font-size:14px;
}

th{
background:#e9f3ed;
}

.filters{
display:flex;
gap:10px;
margin-bottom:10px;
flex-wrap:wrap;
}

.note{
font-size:13px;
color:#666;
margin-top:5px;
}

</style>
</head>


<body>

<div class="container">

<h1>Garcia Property Services Tracker</h1>


<h2>Dashboard</h2>

<div class="grid">

<div class="card">
Total Revenue
<p id="revenue">$0</p>
</div>

<div class="card">
Worker Pay
<p id="workers">$0</p>
</div>

<div class="card">
Expenses
<p id="expenses">$0</p>
</div>

<div class="card">
Profit
<p id="profit">$0</p>
</div>

<div class="card">
Jobs
<p id="jobs">0</p>
</div>

<div class="card">
Work Days
<p id="days">0</p>
</div>

<div class="card">
Avg Per Day
<p id="avgDay">$0</p>
</div>

<div class="card">
Avg Profit Per Day
<p id="avgProfitDay">$0</p>
</div>

<div class="card">
Avg Per Job
<p id="avgJob">$0</p>
</div>

<div class="card">
Unpaid Jobs
<p id="unpaid">$0</p>
</div>

<div class="card">
Highest Job
<p id="highest">$0</p>
</div>

</div>



<h2>Add Job</h2>

<form id="form">

<div class="form-grid">

<input type="date" id="date" required>

<input placeholder="Client name" id="client" required>

<select id="type" required>

<option value="">Job type</option>

<option>Mowing</option>
<option>Mulch</option>
<option>Cleanup</option>
<option>Weeding</option>
<option>Junk Removal</option>
<option>Snow</option>
<option>Other</option>

</select>

<input placeholder="Description" id="desc" required>

<input type="number" placeholder="Revenue" id="rev" required>

<input type="number" placeholder="Worker pay" id="pay">

<input type="number" placeholder="Expenses" id="exp">

<select id="status">

<option>Paid</option>
<option>Unpaid</option>

</select>

</div>

<button class="add">Add Job</button>

</form>

<p class="note">
Data saves in your browser automatically.
</p>



<h2>Jobs</h2>

<div class="filters">

<select id="filterType">

<option>All</option>

<option>Mowing</option>
<option>Mulch</option>
<option>Cleanup</option>
<option>Weeding</option>
<option>Junk Removal</option>
<option>Snow</option>
<option>Other</option>

</select>


<select id="filterStatus">

<option>All</option>

<option>Paid</option>
<option>Unpaid</option>

</select>


<button class="export" id="csv">Export CSV</button>

<button class="clear" id="clear">Clear All</button>

</div>



<table>

<thead>

<tr>

<th>Date</th>
<th>Client</th>
<th>Type</th>
<th>Description</th>
<th>Revenue</th>
<th>Worker</th>
<th>Expenses</th>
<th>Profit</th>
<th>Status</th>
<th></th>

</tr>

</thead>


<tbody id="table">

<tr>

<td colspan="10">No jobs yet</td>

</tr>

</tbody>

</table>


</div>



<script>

let jobs=JSON.parse(localStorage.getItem("jobs"))||[]


function save(){

localStorage.setItem("jobs",JSON.stringify(jobs))

}


function money(n){

return "$"+Number(n).toFixed(2)

}



function profit(j){

return j.rev-j.pay-j.exp

}



function update(){

let rev=0
let pay=0
let exp=0
let prof=0

let unpaid=0

let days=new Set()

let highest=0


jobs.forEach(j=>{

rev+=Number(j.rev)

pay+=Number(j.pay)

exp+=Number(j.exp)

let p=profit(j)

prof+=p

days.add(j.date)

if(j.status=="Unpaid") unpaid+=Number(j.rev)

if(j.rev>highest) highest=j.rev

})


let d=days.size||0

document.getElementById("revenue").innerText=money(rev)

document.getElementById("workers").innerText=money(pay)

document.getElementById("expenses").innerText=money(exp)

document.getElementById("profit").innerText=money(prof)

document.getElementById("jobs").innerText=jobs.length

document.getElementById("days").innerText=d

document.getElementById("avgDay").innerText=money(rev/(d||1))

document.getElementById("avgProfitDay").innerText=money(prof/(d||1))

document.getElementById("avgJob").innerText=money(rev/(jobs.length||1))

document.getElementById("unpaid").innerText=money(unpaid)

document.getElementById("highest").innerText=money(highest)

}



function draw(){

let t=document.getElementById("table")

let type=document.getElementById("filterType").value

let stat=document.getElementById("filterStatus").value


let list=jobs.filter(j=>

(type=="All"||j.type==type)&&
(stat=="All"||j.status==stat)

)


if(list.length==0){

t.innerHTML="<tr><td colspan=10>No jobs</td></tr>"

return

}


list=list.sort((a,b)=>new Date(b.date)-new Date(a.date))


t.innerHTML=list.map(j=>`

<tr>

<td>${j.date}</td>

<td>${j.client}</td>

<td>${j.type}</td>

<td>${j.desc}</td>

<td>${money(j.rev)}</td>

<td>${money(j.pay)}</td>

<td>${money(j.exp)}</td>

<td>${money(profit(j))}</td>

<td>${j.status}</td>

<td>

<button class=delete onclick="del('${j.id}')">

Delete

</button>

</td>

</tr>

`).join("")


update()

}



function del(id){

jobs=jobs.filter(j=>j.id!=id)

save()

draw()

}



document.getElementById("form").onsubmit=e=>{

e.preventDefault()


jobs.push({

id:Date.now(),

date:date.value,

client:client.value,

type:type.value,

desc:desc.value,

rev:Number(rev.value),

pay:Number(pay.value)||0,

exp:Number(exp.value)||0,

status:status.value

})


save()

draw()

form.reset()

}



filterType.onchange=draw

filterStatus.onchange=draw



document.getElementById("clear").onclick=()=>{

if(confirm("delete all?")){

jobs=[]

save()

draw()

}

}



document.getElementById("csv").onclick=()=>{

let rows=[

["date","client","type","description","revenue","worker","expenses","profit","status"]

]


jobs.forEach(j=>{

rows.push([

j.date,
j.client,
j.type,
j.desc,
j.rev,
j.pay,
j.exp,
profit(j),
j.status

])

})


let csv=rows.map(r=>r.join(",")).join("\n")


let blob=new Blob([csv])

let a=document.createElement("a")

a.href=URL.createObjectURL(blob)

a.download="tracker.csv"

a.click()

}



draw()

</script>


</body>

</html>
