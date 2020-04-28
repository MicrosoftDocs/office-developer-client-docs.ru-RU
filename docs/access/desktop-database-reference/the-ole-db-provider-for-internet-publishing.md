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

Объекты [записи](record-object-ado.md) и [потока](stream-object-ado.md) ADO можно использовать с поставщиком Microsoft OLE DB для публикации в Интернете (поставщик публикации в Интернете) для доступа к ресурсам, таким как веб-папки или файлы, обслуживаемые Microsoft FrontPage, и управления ими. С помощью ADO можно указать в качестве источника **записи**, **потока**или [набора записей](recordset-object-ado.md) URL-адрес. После этого вы можете отправлять, загружать, перемещать, копировать и удалять ресурсы, а также напрямую управлять свойствами ресурсов.

Пример кода с использованием **записей** и **потоков** у поставщика публикации в Интернете представлен в статье [Публикация в Интернете](internet-publishing-scenario.md).

Поставщик публикации в Интернете устанавливается вместе с Microsoft Windows 2000. Более ранние версии поставщика публикации в Интернете также доступны в Microsoft Office 2000 и Microsoft Internet Explorer 5,0.

Существует три способа подключения ADO к поставщику публикации в Интернете:

- Укажите "URL =" в строке подключения. Например:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Укажите Мсдаипп. DSO для ключевого слова *provider* строки подключения. Например:
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Укажите Мсдаипп. DSO для свойства [provider](provider-property-ado.md) объекта [Connection](connection-object-ado.md) . Например:
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Если Мсдаипп. DSO явно указан в качестве значения поставщика с помощью ключевого слова строки подключения *поставщика* или свойства **provider** , нельзя использовать "URL =" в строке подключения. В противном случае возникнет ошибка. Вместо этого просто укажите URL-адрес, как показано выше в этом разделе.

Для получения более подробных сведений о поставщике публикации в Интернете обратитесь к разделу [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md)или документации поставщика, поставляемого с исходным приложением, с которым установлен поставщик OLE DB для публикации в Интернете: Windows 2000, Office 2000 или Internet Explorer 5,0.

