param location string = resourceGroup().location
 
param vmName string
 
param adminUsername string
 
param adminPassword string
resource vm 'Microsoft.Compute/virtualMachines@2021-07-01' = {
 
  name: vmName
 
  location: location
 
  properties: {
 
    hardwareProfile: {
 
      vmSize: 'Standard_DS1_v2'
 
    }
 
    storageProfile: {
 
      imageReference: {
 
        publisher: 'Canonical'
 
        offer: 'UbuntuServer'
 
        sku: '22.04-LTS'
 
        version: 'latest'
 
      }
 
      osDisk: {
 
        createOption: 'FromImage'
 
      }
 
    }
 
    osProfile: {
 
      computerName: vmName
 
      adminUsername: adminUsername
 
      adminPassword: adminPassword
 
    }
 
    networkProfile: {
 
      networkInterfaces: [
 
        {
 
          id: "/subscriptions/9f5b21b7-f42e-487d-a6a1-ddf1ccec3633/BH-team/providers/Microsoft.Network/networkInterfaces/mynic"  
 
        }
 
      }
 
    }
 
  }
 
