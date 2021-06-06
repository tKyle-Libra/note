```mermaid
graph TD

  SuperSDK_API

  SuperSDK_API-->init_method

  SuperSDK_API-->call_method

  SuperSDK_API-->appdelegate_method

	 appdelegate_method-->|URL|router

  call_method-->|URL|router

  router-->|router_url|plugins_api_instance

  router-->|router_url|opensdk_api_instance

  opensdk_api_static_register-->plugins_api_instance  

  plugin_a-->|register|opensdk_api_static_register

  plugin_b-->|register|opensdk_api_static_register

  plugin_c-->|register|opensdk_api_static_register

  plugins_api_instance-->|protocol|plugin_a

  plugins_api_instance-->|protocol|plugin_b

  plugins_api_instance-->|protocol|plugin_c
```



