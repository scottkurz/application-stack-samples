# works in dev mode via
  mvn -Pfabric pre-integration-test liberty:dev
# then, since there's no hook into dev mode to stop, do:
  mvn -Pfabric docker:stop
   
# Works in pipeline via:
  mvn -Pfabric pre-integration-test liberty:create liberty:install-feature liberty:start liberty:deploy failsafe:integration-test liberty:stop docker:stop failsafe:verify




