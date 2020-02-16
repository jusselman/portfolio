<?php

if (isset($_POST['submit'])) {
$name = $_POST['name'];
$subject = $_POST['subject'];
$mailFrom = $_POST['mail'];
$message = $_POST['message'];

$mailTo = "joshua@joshusselman.com";
$headers = "From: ".$mailFrom;
$txt = "You have received an e-mail from ".$name.".\n\n".$message;

mail($mailTo, $subject, $txt, $headers);

if( mail($to, $subject, $message, $headers) ){
    echo "Email Sent";
} else {
    echo "The server failed to send the message. Please try again later.";
}

}
?>
