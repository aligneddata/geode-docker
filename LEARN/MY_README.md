# Quick Run
* Init
<pre>
cd composer/
docker-compose up
</pre>
* Re-run
<pre>
docker container start composer_server_1
docker container start composer_locator_1
docker container exec -it composer_locator_1 gfsh

gfsh> connect --locator=locator[10334]
gfsh> list members
gfsh> create region --name=test_region --type=PARTITION
gfsh> list regions
</pre>
docker container stop composer_server_1
docker container stop composer_locator_1
# Logs
* 20241029 Init. Worked.