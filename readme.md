**API Console d'administration Silicom**

Vous trouverez la documentation de l'api sur l'interface Swagger à l'adresse suivante :

Production :<br />
https://api.komodo.ch/index.html

Sandbox :<br />
https://apisandbox.komodo.ch/index.html

Requis :<br />
- DotNet Standard 2.0<br />
- Package System.ComponentModel.Annotations (version 5.0.0.0)

En cas d'erreur :
```
Could not load file or assembly 'System.ComponentModel.Annotations, Version=4.2.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a'
```

Ajouter le code suivant dans l'app.config (version **4.0.0.0**) :
```
<configuration>
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <dependentAssembly>
        <assemblyIdentity name="System.ComponentModel.Annotations" publicKeyToken="b03f5f7f11d50a3a" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.2.1.0" newVersion="4.0.0.0" />
      </dependentAssembly>
    </assemblyBinding>
  </runtime>
</configuration>
```