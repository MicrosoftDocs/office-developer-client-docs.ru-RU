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
# <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="c4204-102">Этап 4. Получение и отображение данных</span><span class="sxs-lookup"><span data-stu-id="c4204-102">Step 4: Receive and Display the Data</span></span>


<span data-ttu-id="c4204-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4204-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="c4204-104">Этап 4. Получение и отображение данных</span><span class="sxs-lookup"><span data-stu-id="c4204-104">Step 4: Receive and Display the Data</span></span>

<span data-ttu-id="c4204-105">На этом этапе создается HTML-файла с внедренным [RDS. DataControl](datacontrol-object-rds.md) объект, указывающий на файл XMLResponse.asp для получения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="c4204-105">In this step you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> <span data-ttu-id="c4204-106">Откройте default.htm в текстовом редакторе, например в Блокноте и добавьте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="c4204-106">Open default.htm with a text editor, such as Windows Notepad, and add the code below.</span></span> <span data-ttu-id="c4204-107">Замените «sqlserver» в URL-имя компьютера сервера.</span><span class="sxs-lookup"><span data-stu-id="c4204-107">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

<span data-ttu-id="c4204-108">Закройте файл default.htm и сохраните его в ту же папку, где был сохранен XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="c4204-108">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> <span data-ttu-id="c4204-109">Откройте /XMLPersist/default.htm*sqlserver*https:// URL-адрес с помощью Internet Explorer версии 4.0 или более поздней версии и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="c4204-109">Using Internet Explorer 4.0 or later, open the URL https://*sqlserver*/XMLPersist/default.htm and observe the results.</span></span> <span data-ttu-id="c4204-110">Данные отображаются в связанной таблице DHTML.</span><span class="sxs-lookup"><span data-stu-id="c4204-110">The data is displayed in a bound DHTML table.</span></span> <span data-ttu-id="c4204-111">Теперь откройте /XMLPersist/XMLResponse.asp*sqlserver*https:// URL-адреса и просмотрите результаты.</span><span class="sxs-lookup"><span data-stu-id="c4204-111">Now open the URL https://*sqlserver*/XMLPersist/XMLResponse.asp and observe the results.</span></span> <span data-ttu-id="c4204-112">XML-код отображается.</span><span class="sxs-lookup"><span data-stu-id="c4204-112">The XML is displayed.</span></span>

