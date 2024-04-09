# csrf
library for csrf protection in PHP. 

example:
<?php
include_once($_SERVER["DOCUMENT_ROOT"] . "/csrf.php");
$csrf = new csrf();
$csrf->generate_token();
?>
<form action="message.php" method="post">
      <input type="text" name="mess">
      <input type="text" name="_token" value=<?=$csrf->getcsrftoken()?>>
      <button type="submit"> sub </button>
</form>
