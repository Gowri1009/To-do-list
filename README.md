<input id="box">
<button onclick="add()">Add</button>
<ul id="container">
    <li>Hello
        <button onclick="dltitem(event)">Delete</button>
    </li>
</ul>

<script>
    var box=document.getElementById("box")
    var ul=document.getElementById("container")
    function add()
    {
        var listitem=document.createElement("li")
        listitem.innerHTML=box.value+"<button onclick='dltitem(event)'>Delete</button>"
        ul.append(listitem)
    }

    function dltitem(event)
    {
        event.target.parentElement.remove()
    }
</script>
