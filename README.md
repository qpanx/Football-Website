


![Uploading Screenshot 2025-05-01 090704.png…]()
![Screenshot 2025-05-01 085223](https://github.com/user-attachments/assets/49c47f61-e3e6-4a19-a098-37474f92b0be)
![Screenshot 2025-05-01 090735](https://github.com/user-attachments/assets/7488ed62-a2f5-45df-b21d-1a7e3faa5cc9)
![Screenshot 2025-05-01 090728](https://github.com/user-attachments/assets/8c002081-c886-4230-9e8c-d9743f8128e7)
![Screenshot 2025-05-01 090720](https://github.com/user-attachments/assets/b40f8416-21aa-4c4b-9b55-f968ad9df508)
![Screenshot 2025-05-01 090740](https://github.com/user-attachments/assets/41813e0b-35c9-42ee-924a-a0979323741a)
![Screenshot 2025-05-01 090713](https://github.com/user-attachments/assets/9a95796a-15d4-4f16-9444-5b60523d5692)
![Screenshot 2025-05-01 090709](https://github.com/user-attachments/assets/4467d7c8-ff0b-46ff-93b3-2b7b474d077d)

![Screenshot 2025-05-01 085216](https://github.com/user-attachments/assets/86b787b6-bd4a-48eb-93b2-9f0434643a80)






## FilaStarter Kit

A Starter Kit For Filament with most basic necessities
pre-configured based on personal preference/requirements.

### Packages

[Laravel](https://github.com/laravel/laravel)  
[Livewire](https://github.com/livewire/livewire)  
[Filament](https://github.com/filamentphp/filament)

#### Packages Installed/Pre-configured

-   Filament Packages

    -   bezhansalleh/filament-shield
    -   jeffgreco13/filament-breezy
    -   z3d0x/filament-logger
    -
    -   awcodes/overlook
    -   awcodes/light-switch
    -   hasnayeen/themes (Default set to Sunset)
    -   joshembling/image-optimizer
    -   njxqlus/filament-progressbar
    -   swisnl/filament-backgrounds
    -   aymanalhattami/filament-slim-scrollbar

-   Other Packages

    -   barryvdh/laravel-ide-helper
    -   barryvdh/laravel-debugbar

-   Notes:

    -   Shield configured to create only these permissions
        `'view','view_any','create','update','delete','delete_any',`

### Installation

#### Create New Project

```fish
composer create-project --prefer-dist raugadh/fila-starter example-app
```

#### Deployment

-   Configure Project.

    -   Update Composer Packages
    -   Add Database Credentials
    -   Add ASSET_PREFIX if deployed application in sub-folder
    -   Link Storage

        ```fish
        php artisan storage:link
        ```

-   Initialize Project

    -   Runs Following in sequence

        ```yaml
        migrate:fresh --force
        shield:generate -all
        db:seed --force
        optimize:clear
        ```

    -   or

        ```fish
          php artisan project:init
        ```

-   Update Permissions and Migrations

    -   Whenever new Resource , Page or migration is Added Run update command to migrate and create permissions.

    -   Runs Following in sequence

        ```yaml
        migrate
        shield:generate -all
        optimize:clear
        ```

    -   or

        ```fish
        php artisan project:update
        ```

-   build vite assets

    ```fish
    npm install && npm run build
    ```

-   Generate IDE:Helper files

    ```yaml
    ide-helper:generate
    ide-helper:models --nowrite
    ide-helper:meta
    ```

    or

    ```fish
    php artisan dev:init
    ``
    ```

#### Enjoy

    Thanks for using this kit, leave a star if you found this useful.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
