---
title: Этап 3. Отправка данных
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 692bf7e1adf561c99ec1e3060578de93fbd1a064
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861885"
---
# <a name="step-3-send-the-data"></a>Этап 3. Отправка данных


**Применимо к**: Access 2013 | Office 2013

## <a name="step-3-send-the-data"></a>Этап 3. Отправка данных

Теперь, когда у вас есть **набор записей**, необходимо отправить его клиенту путем сохранения в формате XML объект ASP **ответа** . Добавьте следующий код в конец XMLResponse.asp:

```vb 
 
  Response.ContentType = "text/xml" 
  Response.Expires = 0 
  Response.Buffer = False 
 
 
  Response.Write "<?xml version='1.0'?>" & vbNewLine 
  adoRec.save Response, adPersistXML 
  adoRec.Close 
  Set adoRec=Nothing 
%> 
```

Обратите внимание на то, что объект ASP **ответа** указан как назначения для метода **записей** [Сохранить](save-method-ado.md) . Конечный метод **Save** может быть любой объект, который поддерживает интерфейс **IStream** , например, объект ADO [потока](stream-object-ado.md) или имя файла, который включает в себя полный путь к которой должен быть сохранен **набора записей** .

Сохраните и закройте XMLResponse.asp перед переходом к следующему шагу. Также скопируйте файл adovbs.inc из C:\\Program Files\\общие файлы\\системы\\Ado папки в ту же папку, где у вас есть файл XMLResponse.asp.

### <a name="next-step"></a>Дальнейшие действия

[Шаг 4: Получение данных](step-4-receive-and-display-the-data.md)

