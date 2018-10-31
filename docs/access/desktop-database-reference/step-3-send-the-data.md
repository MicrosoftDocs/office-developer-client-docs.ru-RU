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
# <a name="step-3-send-the-data"></a><span data-ttu-id="5aeab-102">Этап 3. Отправка данных</span><span class="sxs-lookup"><span data-stu-id="5aeab-102">Step 3: Send the Data</span></span>


<span data-ttu-id="5aeab-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5aeab-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="5aeab-104">Этап 3. Отправка данных</span><span class="sxs-lookup"><span data-stu-id="5aeab-104">Step 3: Send the Data</span></span>

<span data-ttu-id="5aeab-105">Теперь, когда у вас есть **набор записей**, необходимо отправить его клиенту путем сохранения в формате XML объект ASP **ответа** .</span><span class="sxs-lookup"><span data-stu-id="5aeab-105">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> <span data-ttu-id="5aeab-106">Добавьте следующий код в конец XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="5aeab-106">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

<span data-ttu-id="5aeab-107">Обратите внимание на то, что объект ASP **ответа** указан как назначения для метода **записей** [Сохранить](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5aeab-107">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="5aeab-108">Конечный метод **Save** может быть любой объект, который поддерживает интерфейс **IStream** , например, объект ADO [потока](stream-object-ado.md) или имя файла, который включает в себя полный путь к которой должен быть сохранен **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5aeab-108">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

<span data-ttu-id="5aeab-109">Сохраните и закройте XMLResponse.asp перед переходом к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="5aeab-109">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="5aeab-110">Также скопируйте файл adovbs.inc из C:\\Program Files\\общие файлы\\системы\\Ado папки в ту же папку, где у вас есть файл XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="5aeab-110">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

### <a name="next-step"></a><span data-ttu-id="5aeab-111">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5aeab-111">Next step</span></span>

[<span data-ttu-id="5aeab-112">Шаг 4: Получение данных</span><span class="sxs-lookup"><span data-stu-id="5aeab-112">Step 4: Receive the Data</span></span>](step-4-receive-and-display-the-data.md)

