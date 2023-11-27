# Ziggy Routes Auto Generate

This Command Generate All Files In Routes Folder To Ziggy Json File And Make Auto Generate If Any Route Changed .

## Installation

- Open vite.config.js Then At The Top Of File Add

```bash
import { exec } from "node:child_process";
```

- And At The End Of Plugins Add

```bash
{
    name: "ziggy",
    enforce: "post",
    handleHotUpdate({ server, file }) {
        if (file.includes("/routes/") && file.endsWith(".php")) {
            exec(
                "php artisan ziggy:generate",
                (error, stdout) =>
                    error === null &&
                    console.log(`Ziggy Routes Generated Successfully !`)
            );
        }
    },
},
```

- Congratulations You Have Now Auto Generated For Routes Folder

## Links

* [LinkedIn](https://www.linkedin.com/in/a-mohamed-nader/)
* [Whatsapp](https://wa.me/+201098683990)
* [Facebook](https://www.facebook.com/httpsnader0)
* [Instagram](https://www.instagram.com/httpsnader0)
