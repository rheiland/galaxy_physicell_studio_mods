# galaxy_physicell_studio_mods

Modifications needed to a local Galaxy server to allow the creation of the PhysiCell Studio interactive tool.

Need to:
```
cp galaxy.yml <path-to-galaxy>/config/.
cp tool_conf.yml <path-to-galaxy>/config/.
cp interactivetool_pcstudio.xml <path-to-galaxy>/tools/interactive/.
```
and `tool_conf.yml` needs to have the correct name of the new tool, e.g., `interactivetool_pcstudio.xml`