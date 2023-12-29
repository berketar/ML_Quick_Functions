The helper functions python script can be called using the following code snippet from any python application.

This code will create a helper_functions.py script on your folder with the wb permissions.

You may change the name of the created file from with open line if you need a different name on your folder.

import requests

from pathlib import Path

if Path("helper_functions.py").is_file():
    print("helper functions already exists in your folder, why bother?")

else:
    print("downloading the helper functions from berketars repo")
    request=requests.get("https://raw.githubusercontent.com/berketar/ML_Quick_Functions/main/dbourkehelper.py")
    with open("helper_functions.py","wb") as f:
        f.write(request.content)


The script is copied from mrdbourke/pytorch-deep-learning repository.
