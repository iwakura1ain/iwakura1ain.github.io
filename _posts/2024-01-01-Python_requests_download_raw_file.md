
# Table of Contents

1.  [Python requests download raw file](#org2c5c485)


<a id="org2c5c485"></a>

# Python requests download raw file

    import requests
    import shutil
    
    r = requests.get(settings.STATICMAP_URL.format(**data), stream=True)
    if r.status_code == 200:
        with open(path, 'wb') as f:
            r.raw.decode_content = True
            shutil.copyfileobj(r.raw, f)   

