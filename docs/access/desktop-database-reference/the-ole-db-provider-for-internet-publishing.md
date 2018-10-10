---
title: The OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9f8fbed638c07e55b3ecb1730633dceee2b5c7e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480161"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a>The OLE DB Provider for Internet Publishing


**Применимо к**: Access 2013 | Office 2013

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
> <P>Если Msdaipp.dso явным образом указаны как значение поставщика, с ключевым словом строки подключения <EM>поставщика</EM> или свойство <STRONG>поставщика</STRONG> нельзя использовать «URL-адрес =» в строке подключения. В противном случае возникнет ошибка. Вместо этого просто укажите URL-адрес, как показано выше.</P>



Более подробные сведения о поставщике публикации Интернет отображаться [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)или документации поставщика, входящие в состав исходное приложение, с которым была поставщика OLE DB для публикации Интернет установленные: Windows 2000, Office 2000 или Internet Explorer версии 5.0.

