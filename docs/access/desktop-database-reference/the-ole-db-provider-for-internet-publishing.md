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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699130"
---
# <a name="ole-db-provider-for-internet-publishing"></a>Поставщик OLE DB для публикации в Интернете

**Применимо к**: Access 2013, Office 2013

Объекты ADO [записи](record-object-ado.md) и [потока](stream-object-ado.md) можно использовать с поставщик Microsoft OLE DB для публикации Интернет (публикации Интернета) для доступа и работы с ресурсами, такие как веб-папок или файлов, размещенных в Microsoft FrontPage. С помощью ADO можно указать источник **записи**, **потока**или [набора записей](recordset-object-ado.md) URL-адрес. Вы можно отправить, загрузить, переместить, скопировать и удаления ресурсов или непосредственного управления свойства ресурса.

Пример кода с помощью **записей** и **потоков** с поставщиком публикации Интернета, содержатся в [Сценарий публикации в Интернете](internet-publishing-scenario.md).

Поставщик публикации Интернет устанавливается вместе с Microsoft Windows 2000. Более ранних версий службу публикации в Интернете, также доступны с помощью Microsoft Office 2000 и Microsoft Internet Explorer версии 5.0.

Существует три способа подключения ADO службу публикации в Интернете:

- Укажите «URL-адрес =» в строке подключения. Пример:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Укажите Msdaipp.dso для *поставщика* ключевое слово строки подключения. Пример:
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Укажите Msdaipp.dso для [поставщика](provider-property-ado.md) свойства объекта [подключения](connection-object-ado.md) . Пример:
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Если Msdaipp.dso явным образом указаны как значение поставщика, с ключевым словом строки подключения *поставщика* или свойство **поставщика** нельзя использовать «URL-адрес =» в строке подключения. В противном случае возникнет ошибка. Вместо этого просто укажите URL-адрес, как показано выше в этом разделе.

Более подробные сведения о поставщике публикации Интернет отображаться [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)или документации поставщика, входящие в состав исходное приложение, с которым была поставщика OLE DB для публикации Интернет установленные: Windows 2000, Office 2000 или Internet Explorer версии 5.0.

