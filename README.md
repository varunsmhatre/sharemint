# ShareMint: A Python Package for Easy SharePoint Interaction

ShareMint is a Python package that provides a higher-level interface to interact with SharePoint folders and files. Built on top of the Office365-REST-Python-Client, ShareMint aims to simplify SharePoint website folder interaction.(https://github.com/vgrem/Office365-REST-Python-Client)


# Installation
You can easily install ShareMint using pip:

```
pip install sharemint
```

You can also find the package on PyPI at: https://pypi.org/project/sharemint/


# Usage
To use ShareMint, you first need to import it using: 

```
from sharemint import ShareMint

my_website = ShareMint(client_id=client_id, client_secret_key=client_secret, site_url=site_url)
```

E.g. site_url: https://mydomainnamexyz.sharepoint.com/sites/website_name

To generate Client Credentials for your SharePoint Website, please check the below resource metioned below:

URL: https://faun.pub/quick-etl-with-python-part-1-download-files-from-sharepoint-online-40bf23711662


# Supported Methods
ShareMint currently supports the following methods:

* file_exists(file_site_path) -> bool ( Tells if a file exists in SharePoint Folder ) 

* download_file(file_site_path, save_folder_path) -> str ( Downloads file to local folder )

* upload_file(device_file_path, sharepoint_folder_path) -> None ( Uploads File to a SharePoint Folder )

* delete_file(file_path) -> None ( Deletes a file from a SharePoint Folder )

* get_updated_files_path(created_datetime_utc: str|datetime ) -> list ( Return list of files created>=created_datetime_utc )

* download_folder(self, site_folder_path:str, download_folder_path=str) -> str ( Downloads folder from sharepoint and returns the downloaded folder path )
