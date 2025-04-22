# galaxy_physicell_studio_mods

Modifications needed to a local Galaxy server to allow the creation of the PhysiCell Studio interactive tool.

Need to:
```
cp galaxy.yml <path-to-galaxy>/config/.
# or, alternatively, perhaps it is sufficient to just use the one in the galaxy server, i.e.:
(base) heiland@yoga:~/dev/galaxy-24.2.3/config$ cp galaxy.yml.interactivetools galaxy.yml

cp tool_conf.xml <path-to-galaxy>/config/.
cp interactivetool_pcstudio.xml <path-to-galaxy>/tools/interactive/.
```
and `tool_conf.yml` needs to have the correct name of the new tool, e.g., `interactivetool_pcstudio.xml`
