git-explorer
============

> view all DAG nodes in the .git/objects folder

Purpose
-------
When we run `git log ...` we only see the commits.  But if we open the `.git` folder and cruise through the `objects` folder, we see much more content in there.  This tool allows you to view all the DAG nodes and visualize their relationships and content.


How to Use
----------

1. Specify the git repo to examine: Inside the `src` folder, create an `env.json` file that looks like this:

   ```
   {
     "gitRepo": "/path/to/your/repo"
   }
   ```

   Note that this is to the root repo folder, the one with the .git folder inside it, not the .git folder itself.

2. `npm install` or `yarn install`

3. `npm start`

4. Browse to http://localhost:3000/

   By default, it shows all the commits in a big blob. Click on the buttons above to arrange the nodes or show more features.

   Click on a dot on the left to show the content of that DAG node on the right.

### Issue:
OS Windows 10 

npm: '10.8.3'

#### Error:
 
$ npm start

> git-explorer@0.0.1 prestart
> npm run build


> git-explorer@0.0.1 prebuild
> tslint -c tslint.json -p tsconfig.json --fix


> git-explorer@0.0.1 build
> tsc

src/gitter/inject-refs.ts:30:11 - error TS18046: 'err' is of type 'unknown'.

30       if (err.code === 'ENOENT') {
             ~~~
             
Found 1 error in src/gitter/inject-refs.ts:30

#### Fix:

https://stackoverflow.com/a/69445095/2961448 

you need to put it like this under compilerOptions

"compilerOptions": {
    "useUnknownInCatchVariables": false
  }

License
-------

License: MIT, Copyright Richardson & Sons, LLC
