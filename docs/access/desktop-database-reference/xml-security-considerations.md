---
title: XML Security Considerations
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 648e7980be19f8af39cdb5e19858ba1ffd16518e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308248"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="d1ff3-102">Рекомендации по безопасности XML</span><span class="sxs-lookup"><span data-stu-id="d1ff3-102">XML security considerations</span></span>


<span data-ttu-id="d1ff3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1ff3-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="d1ff3-104">XML Security Considerations</span><span class="sxs-lookup"><span data-stu-id="d1ff3-104">XML Security Considerations</span></span>

<span data-ttu-id="d1ff3-105">Методы ADO **Save** и **Open** в **объекте Recordset** не считаются безопасными операциями для запуска в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d1ff3-105">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer.</span></span> <span data-ttu-id="d1ff3-106">Таким образом, если эти методы используются в коде сценария, который работает в приложении или в средстве управления, который находится в браузере, конфигурация безопасности браузера будет действовать на его поведение.</span><span class="sxs-lookup"><span data-stu-id="d1ff3-106">Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="d1ff3-107">Internet Explorer 5 предоставляет ограничения безопасности для таких операций по умолчанию в зонах Интернета.</span><span class="sxs-lookup"><span data-stu-id="d1ff3-107">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones.</span></span> <span data-ttu-id="d1ff3-108">В этой конфигурации набор **записей** не может получить доступ к локальной файловой системе на клиенте или получить доступ к источникам данных за пределами домена сервера, с которого была загружена страница.</span><span class="sxs-lookup"><span data-stu-id="d1ff3-108">Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded.</span></span> <span data-ttu-id="d1ff3-109">В частности, при запуске в  хост-сервере браузера набор записей можно сохранить обратно в файл, только если он находится на том же сервере, с которого была загружена страница.</span><span class="sxs-lookup"><span data-stu-id="d1ff3-109">Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded.</span></span> <span data-ttu-id="d1ff3-110">Аналогичным образом можно открыть  набор записей, загрузив его из файла, только если этот файл находится на том же сервере, с которого была загружена страница.</span><span class="sxs-lookup"><span data-stu-id="d1ff3-110">Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="d1ff3-111">Дополнительные сведения о безопасности в Internet Explorer см. в технической статье "Проблемы безопасности ADO и RDS в Microsoft Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="d1ff3-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>

