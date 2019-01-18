---
title: Рекомендации по безопасности XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 648e7980be19f8af39cdb5e19858ba1ffd16518e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706340"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="c5262-102">Рекомендации по безопасности XML</span><span class="sxs-lookup"><span data-stu-id="c5262-102">XML security considerations</span></span>


<span data-ttu-id="c5262-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5262-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="c5262-104">Рекомендации по безопасности XML</span><span class="sxs-lookup"><span data-stu-id="c5262-104">XML Security Considerations</span></span>

<span data-ttu-id="c5262-105">Методы ADO **сохранения** и **открытия** в объекте **набора записей** , не считаются безопасных операций для запуска в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5262-105">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer.</span></span> <span data-ttu-id="c5262-106">Таким образом Если эти методы используются в коде скрипта, который работает в приложения или элемента управления, которая размещается в браузере, настройка безопасности обозревателя будут иметь влияет на поведение.</span><span class="sxs-lookup"><span data-stu-id="c5262-106">Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="c5262-107">Internet Explorer 5 обеспечивает ограничения безопасности для таких операций по умолчанию в зоне Интернета.</span><span class="sxs-lookup"><span data-stu-id="c5262-107">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones.</span></span> <span data-ttu-id="c5262-108">В разделе этой конфигурации **набора записей** невозможно сделать никакого доступа к локальной файловой системе на стороне клиента или получить доступ к источникам данных за пределами домена сервера, из которой был загружен страницы.</span><span class="sxs-lookup"><span data-stu-id="c5262-108">Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded.</span></span> <span data-ttu-id="c5262-109">В частности при выполнении внутри узла браузера **записей** можно сохранить обратно в файл только в том случае, если это на том же сервере, из которой был загружен страницы.</span><span class="sxs-lookup"><span data-stu-id="c5262-109">Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded.</span></span> <span data-ttu-id="c5262-110">Аналогично можно открыть **записей** путем загрузки из файла, только если этот файл находится на том же сервере, из которой был загружен страницы.</span><span class="sxs-lookup"><span data-stu-id="c5262-110">Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="c5262-111">Дополнительные сведения о безопасности в Internet Explorer см «ADO и проблемы безопасности служб удаленных рабочих СТОЛОВ в Microsoft Internet Explorer.»</span><span class="sxs-lookup"><span data-stu-id="c5262-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>

