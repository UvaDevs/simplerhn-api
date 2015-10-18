## SimplerHN API
SimplerHN cuenta con una API HTTP para enviar SMS de manera muy simple.

Petición HTTP debe realizarse por HTTP Seguro (HTTPS) a travez del metodo GET. La URL de destino debe ser.

    https://simplerhn.com/api/sms/enviar

#### Parametros GET

Es necesario incluir en la petición HTTP 3 parametros obligatorios. Estos parametros son.

1. smstel - Numero de teléfono de destino.
2. smstxt - Contenido del SMS.
3. usrapi - Llave API

#### Ejemplo

Como ejemplo mas simple, a continuación se muestra una URL en su estructura final para ser enviada por el Metodo HTTP GET.

    https://simplerhn.com/api/sms/enviar?smstel=Mensaje
    AMisClientes&smstxt=0050499929922&usrapi=755936d0710e12r5
    a8380d123495b0645

#### Respuestas

La respuesta obtenida despues de la ejecución de la petición variara, a continuación se muestran las posibles respuestas en formato JSON.

###### Mensaje Enviado Exitosamente.

    {error: null,data: null}

###### Error Enviando Mensaje

    {
      error:[
        {
          Id: "[codigo]",
          Description: "[descripcion]",
          Type: "[type]"
        }
      ],
      data: null
    }

##### Códigos de error

- 1033 Numero de telefono incorrecto
- 1025 Error creando proceso.
- 1024 Saldo insuficiente para realizar envio.
- 1017 Usuario no encontrado.
