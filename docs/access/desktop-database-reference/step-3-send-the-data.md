---
title: 'Шаг 3: Отправка данных'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3e6bfd6fe3b6727055eb264b1261b13d7a5a0b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479980"
---
# <a name="step-3-send-the-data"></a>Шаг 3: Отправка данных


**Применимо к**: Access 2013 | Office 2013

## <a name="step-3-send-the-data"></a>Шаг 3: Отправка данных

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

**Далее** [Шаг 4: получение данных](step-4-receive-and-display-the-data.md)

