## Azure VMs

```
Get-AzVmImageSku -Location 'westeurope' -Offer 'UbuntuServer' -PublisherName 'Canonical' 
```

The images on Azure are not really the latest greatest….

You need to update your repository targets to the Eoan Ermine (19.10) release of Ubuntu. This can be done like so:
```
sudo sed -i -e 's|disco|eoan|g' /etc/apt/sources.list
sudo apt update
```