## Error docker windows Docker.ApiServices.WSL2.Wsl kernel Update Not Installed Exception

 - Abra o powershell como administrador
 - Execute o comando Enable-WindowsOptionalFeature -Online -FeatureName $("VirtualMachinePlatform","Microsoft-Windows-Subsystem-Linux")
 - Entre nesse link da Microsoft https://docs.microsoft.com/pt-br/windows/wsl/install-manual baixe o pacote de atualização do kernel do linux provavelmente estara na etapa 4
 - Instale o pacote 
 - Reinicie a maquina
