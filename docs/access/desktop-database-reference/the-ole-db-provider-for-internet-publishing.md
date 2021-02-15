---
title: The OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314058"
---
# <a name="ole-db-provider-for-internet-publishing"></a>Поставщик OLE DB для публикации в Интернете

**Область применения**: Access 2013, Office 2013

Объекты ADO [Record](record-object-ado.md) и [Stream](stream-object-ado.md) можно использовать с поставщиком Microsoft OLE DB для публикации в Интернете (Internet Publishing Provider) для доступа к ресурсам, таким как веб-папки или файлы, обслуживаемые Microsoft FrontPage, и управлять ими. С помощью ADO можно указать источник **record,** **Stream** или [Recordset в](recordset-object-ado.md) качестве URL-адреса. Затем можно загрузить, скачать, переместить, скопировать и удалить ресурсы или напрямую управлять свойствами ресурсов.

Пример кода с использованием **записей** и потоков с поставщиком интернет-публикации см. в сценарии  [публикации в Интернете.](internet-publishing-scenario.md)

Поставщик публикации в Интернете устанавливается вместе с Microsoft Windows 2000. Более ранние версии поставщика интернет-публикации также доступны в Microsoft Office 2000 и Microsoft Internet Explorer 5.0.

Существует три способа подключения ADO к поставщику интернет-публикации:

- Укажите "URL=" в строке подключения. Например:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Укажите Msdaipp.dso для ключевого слова *Provider* строки подключения. Например:
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Укажите Msdaipp.dso для свойства [Provider](provider-property-ado.md) объекта [Connection.](connection-object-ado.md) Например:
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Если Msdaipp.dso явным образом указан в качестве значения  поставщика с помощью ключевого слова "Строка подключения поставщика" или свойства **Provider,** в строке подключения нельзя использовать "URL=". В этом случае произойдет ошибка. Вместо этого просто укажите URL-адрес, как показано ранее в этом разделе.

Дополнительные сведения о поставщике публикации в Интернете см. в документации поставщика [Microsoft OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)для публикации в Интернете или в документации поставщика, предоставленной исходным приложением, с которым установлен поставщик OLE DB для публикации в Интернете: Windows 2000, Office 2000 или Internet Explorer 5.0.

