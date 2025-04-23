# galaxy_physicell_studio_mods

Modifications needed to a local Galaxy server to allow the creation of the PhysiCell Studio interactive tool.

Need to:
```
cp galaxy.yml <path-to-galaxy>/config/.
cp job_conf.yml <path-to-galaxy>/config/.
cp tool_conf.xml <path-to-galaxy>/config/.
cp interactivetool_pcstudio.xml <path-to-galaxy>/tools/interactive/.
```
and `tool_conf.yml` needs to have the correct name of the new tool, e.g., `interactivetool_pcstudio.xml`

Start Galaxy for the first time with:
```
sh run.sh
```

Afterwards, you can start Galaxy with:
```
source .venv/bin/activate
galaxyctl start [restart | stop | status]
```
in which case Galaxy web server logs will be in
`./database/gravity/log/gunicorn.log`

Once Galaxy is started, you can access it at `http://localhost:8080/`. To start
the PhysiCell Studio interactive tool, find it under the "Interactive Tools"
section in the Galaxy interface. After you run the tool, if you try to access it
but get 'Proxy target missing', try restarting the Galaxy proxy server and
accessing the tool again.

```
galaxyctl restart gx-it-proxy
```
