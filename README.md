### without docker

#### Berfore hand

* Download [Node.JS V9.11.2](https://nodejs.org/dist/v9.11.2/node-v9.11.2-x64.msi)
  * Add `C:\Program Files\nodejs` to PATH
  * Download Angular CLI

    ```bash
    npm -g i @angular/cli@7.3.9
    ```

* Download [MongoDB Server](https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi)

* Setup Virtualenv and install python requirements

```sh
python -m venv .venv
Set-ExecutionPolicy Unrestricted -Scope Process
.venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
```

#### Update Frontend Dist

Open new terminal to process this.

* Run Development mode

```sh
cd frontend
npm install
```

* Take Production build

```sh
ng build --prod --optimize
ng serve

```sh
* run app

```sh
python run.py
```

* Open <http://localhost:4200/>