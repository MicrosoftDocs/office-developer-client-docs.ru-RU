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

Объекты ADO [Record](record-object-ado.md) и [Stream](stream-object-ado.md) можно использовать с поставщиком microsoft OLE DB для интернет-публикации (поставщик публикаций в Интернете) для доступа к ресурсам, таким как веб-папки или файлы, обслуживаемые Microsoft FrontPage. С помощью ADO можно указать источник записи, **потока** или [набор](recordset-object-ado.md) записей для URL-адреса. Затем вы можете загружать, скачивать, перемещать, копировать и удалять ресурсы или напрямую управлять свойствами ресурсов.

Например, **код,** использующий записи **и Потоки** с поставщиком интернет-публикаций, см. сценарий [публикации в Интернете.](internet-publishing-scenario.md)

Поставщик интернет-публикаций установлен с microsoft Windows 2000. Более ранние версии поставщика интернет-публикаций также доступны с Microsoft Office 2000 и Microsoft Internet Explorer 5.0.

Существует три способа подключения ADO к поставщику интернет-публикаций:

- Укажите "URL=" в строке подключения. Пример.
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Укажите msdaipp.dso для ключевого слова *Поставщика* строки подключения. Пример.
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Укажите msdaipp.dso для свойства [Поставщика](provider-property-ado.md) объекта [Подключения.](connection-object-ado.md) Пример.
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Если msdaipp.dso явно указывается в качестве значения поставщика  либо с ключевым  словом строки подключения поставщика, либо с свойством Provider, вы не можете использовать URL=" в строке подключения. Если это произойдет, произойдет ошибка. Вместо этого просто укажите URL-адрес, как показано ранее в этом разделе.

Дополнительные сведения о поставщике интернет-публикаций см. в публикации [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)или документации поставщика, предоставленной с исходным приложением, с которым установлен поставщик OLE DB для интернет-публикации: Windows 2000, Office 2000 или Internet Explorer 5.0.

