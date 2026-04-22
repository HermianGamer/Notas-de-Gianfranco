`wget` es una potente herramienta de línea de [[command]] en Linux, desarrollada por el Proyecto GNU, diseñada para descargar [[File]]s de internet de forma no interactiva a través de HTTP, HTTPS y FTP. Permite descargas recursivas, reanudar transferencias interrumpidas y operar en segundo plano, siendo ideal para scripts y automatización. ![Hostinger|20](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAE7ElEQVRoge2YX4hUVRzHP+fOtqZmrZYPQVAv9aS7MxeKSsx8uFfTNFLKzCJFIbXONewhNIgoKJJQ917dULS/Uhq0aouxcycKozJIz6hBUBkEpQViCaa72s799XCdmll3Z2d2Znf2YT/DPNy555z5fe89v9/5/X6KArRj1gPjFOoNP5M6yTCgHTMFeAF4D2VlgjDZXcl8q9f1ZOB5QfZqxyzXbnZSrQwdwIaZwLtItFM75l49Kzumksl9cTvQhki7dswiz81OqIWlJRCgCXgU2EskO7VjZnhutnGgif0JAGgEZgBvichu7Zg5nmvG1sbekjQBS4C9IrJDO2a6LiGklIA8Y4E5wG4R3tZOdkapBWvIROBxYB8i27Vjpnmuuar3oHIE5JkAPAzSjkibdkyqVpYCqsS9ScATwH4RtnmOmVp4sxIBhQsuB15aM/to2c5WA64Hlkks5j8GIyDPuCrnFyIVjE0UXtTKgLoxKqDejAqoEaXCaElGioBKolARdRegFCeB/cC5wcxvqOK/ExLJNZ5jiuKyUgW7QS4/Wim8DygiLLpaO1Pih/YZ7WY1Ih8Da4FpwBUpw1AIaBGRfUCOgj0sIlduh2JNIPSQo1M7ZleQsU8FYaob6NCu+RphMfA0cBtl+EY1ApqAu6uYfw+wSDumTSna/dD+KwjtM8AWzzWdIqwiTuYml1qknj6QAGygTYSPtGMWaCc7HsAP7RNY6jlgAdAOdPW3SDVvoFY0Eldkd4CktWO2oNRXQTp1CfjSc0xWYD7wTDymeFuNBAF5xhM/8ZmXK8E2rMQxP91yHvhAu9nPEVlBr7cxkgTkmUicrt9PlNulnewOLOvHIN3yh+eaV4GrCwcXCVBwQOAMEA2fvf1y2T9lCiK/AX/7oZ0DztfTqJrTb5zVbrZBQMRSkaUgQQNKIjZ1Ng/62B8K+hTgzTuu5GLPXQgLieNwD/G2kjp/FXAoyNif5m0t8oE1s48lWjtbcn5Hs3iuOSKxw2hgFnF3YiSwGehbQJTLLdGO6VbK6vDDZBfwmXbNNwgOsZDpxHF7xNA7jNrASpGoXTtms1iJw0G65QKw33OzB0VkAbAaSNKruK4XvVMJAcYAi4F9Ksq9rN3szQB+mDobZOw3lWI+sA74iSry+FpRKhe6EViHSId2zArPNdcB+KF9qiFhva7ibt0GYFi62P0x0EmsgKnAVhEWasdsVJY6uKkzeQk44blH14vIHpClwK1c+UbKKRWvJW4mD8q3yk0lGoHZwJ0SyR7PMQEW3/vpZARkn3LNMYSEIv78H/UGJEfsT2nghkHYX3Eu1AQ8KTCLiNfWzj2+feOB5mhraEcMMv3QjumhDjXxLcBDuVw0nL3RPql7UV8towLqzaiAejNSBNSsN3qaOPcfNhSqi7iMHRRFApSiDVgBHAL+qc60Mg1Q6mfgMWAn8GfF8wsv/NA+G2Tsd0A9QJz/HyE+7oeMzWEyCjL2YWVZq4nbKh9SQaO3Tx8IMqnTQcbephTzgGeB7xjiToWfTl4KMvZBpdRS4nT+E0p05PKUdGI/tH8PMnYrSs0F1gM/MMQ1gB+muoKMfUAp9QiwDPiCEtu5rCgUhKlfLYsNKO4DXgR+YeiFnAsy9h6UehBYBXzb17iKw5fnGoXQLArbUur91nTqYrXGloN2zE3ASuBCkLFfyf/+L+aIzcGFD3oBAAAAAElFTkSuQmCC)Hostinger +4

**Uso Básico y Ejemplos:**

- **Descargar un archivo:** `wget <URL>`.
- **Descargar y renombrar:** `wget -O nombre_nuevo.zip <URL>`.
- **Reanudar descarga interrumpida:** `wget -c <URL>`.
- **Descargar en segundo plano:**
    
     `wget -b <URL>`.
    

- **Descargar todo un sitio web (recursivo):** `wget -r <URL>`. ![GNU|20](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.gnu.org&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)GNU +4

**Instalación:**  
`wget` suele venir preinstalado, pero si no, se puede instalar en distribuciones basadas en Debian/Ubuntu con:  
`sudo apt-get install wget`. DigitalOcean

Para más información, se puede consultar el manual con el comando `man wget`