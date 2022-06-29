# Unqork Customer - Node Script

`Current Version: 0.0.1`

Script to serve local customer.css and customer.js files at correct path and port to use with Unqork remoteRootCustomer.

## Install Dependencies:

```
npm install
```

## Usage

Place files into `/dist/` folder using the following folder structure and naming convention:

```
/dist/[client-name]/styles/[theme-name]
```

This should match up with the environment and theme name that is being loaded in with `remoteRootCustomer`

```
?remoteRootCustomer=http://localhost:3002/[client-name]/&style=[theme-name]
```

Run the script using npm

```
npm run dev
```

The files should now be served at the correct location.

## Example

Unqork-v2 base style has been loaded in as an example at the correct path. To test your setup, run the script with `npm run dev` and load the Styles UI Kit V2 using the local Unqork Theme

```
https://styles-stagingx.unqork.io/?remoteRootCustomer=http://localhost:3002/unqork/&style=unqork-v2#/display/61675971974e7c01809ea779
```

## Troubleshooting

If you are getting 404 errors, most likely you do not have the paths matching between your remoteRootCustomer string and your `/dist/` folder.
