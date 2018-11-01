---
title: Этап 4. Получение и отображение данных
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03a089e600799e1ac5fa85886ee6a16e1dd86026
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869080"
---
# <a name="step-4-receive-and-display-the-data"></a>Этап 4. Получение и отображение данных


**Применимо к**: Access 2013, Office 2013

## <a name="step-4-receive-and-display-the-data"></a>Этап 4. Получение и отображение данных

На этом этапе создается HTML-файла с внедренным [RDS. DataControl](datacontrol-object-rds.md) объект, указывающий на файл XMLResponse.asp для получения **набора записей**. Откройте default.htm в текстовом редакторе, например в Блокноте и добавьте приведенный ниже код. Замените «sqlserver» в URL-имя компьютера сервера.

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

Закройте файл default.htm и сохраните его в ту же папку, где был сохранен XMLResponse.asp. Откройте /XMLPersist/default.htm*sqlserver*https:// URL-адрес с помощью Internet Explorer версии 4.0 или более поздней версии и просмотрите результаты. Данные отображаются в связанной таблице DHTML. Теперь откройте /XMLPersist/XMLResponse.asp*sqlserver*https:// URL-адреса и просмотрите результаты. XML-код отображается.

