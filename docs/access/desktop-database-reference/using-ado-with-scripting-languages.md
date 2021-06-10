---
title: Using ADO with Scripting Languages
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312043"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="80c23-102">Использование ADO со скриптовыми языками</span><span class="sxs-lookup"><span data-stu-id="80c23-102">Using ADO with scripting languages</span></span>


<span data-ttu-id="80c23-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80c23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80c23-104">В среде скриптов ADO позволяет выставлять данные с помощью сценариев на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="80c23-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="80c23-105">В этом сценарии ADO— поставщик OLE DB, который он использует, и все другие компоненты, необходимые для ссылки на данный хранилище данных, устанавливаются на сервере с службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="80c23-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="80c23-106">С ASP (ASP) ADO — это компонент, на который ссылается скрипт, который может создавать HTML, например.</span><span class="sxs-lookup"><span data-stu-id="80c23-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="80c23-107">Этот HTML-контент можно передать через HTTP в клиентский веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="80c23-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="80c23-108">С помощью скриптов веб-сайт может отправлять действия обратно в серверный сценарий, что позволяет обновлять, пересекать или просматривать определенные данные.</span><span class="sxs-lookup"><span data-stu-id="80c23-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="80c23-109">Источники данных ODBC</span><span class="sxs-lookup"><span data-stu-id="80c23-109">ODBC Data Sources</span></span>

<span data-ttu-id="80c23-110">Одно заметное различие между скриптами и кодом ADO без скриптов — это источник данных ODBC, если он используется.</span><span class="sxs-lookup"><span data-stu-id="80c23-110">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</span></span> <span data-ttu-id="80c23-111">Для приложений, не создающих сценарии, можно создать DSN пользователя в администраторе источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="80c23-111">For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</span></span> <span data-ttu-id="80c23-112">Для скриптов, работающих под IIS, необходимо создать систему DSN; в противном случае скрипты не распознают созданный источник данных.</span><span class="sxs-lookup"><span data-stu-id="80c23-112">For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created.</span></span> <span data-ttu-id="80c23-113">Это относится к любому приложению для скриптинга ADO с помощью поставщика DB Microsoft OLE для ODBC через Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="80c23-113">This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="80c23-114">Ссылки на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="80c23-114">Referencing the ADO Library</span></span>

<span data-ttu-id="80c23-115">N/A с языками скриптов.</span><span class="sxs-lookup"><span data-stu-id="80c23-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="80c23-116">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="80c23-116">Handling events</span></span>

<span data-ttu-id="80c23-117">N/A с языками скриптов.</span><span class="sxs-lookup"><span data-stu-id="80c23-117">N/A with scripting languages.</span></span>

<span data-ttu-id="80c23-118">В следующих темах содержатся более конкретные сведения об использовании ADO с языками скриптов:</span><span class="sxs-lookup"><span data-stu-id="80c23-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="80c23-119">JScript ADO Programming</span><span class="sxs-lookup"><span data-stu-id="80c23-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="80c23-120">VBScript ADO Programming</span><span class="sxs-lookup"><span data-stu-id="80c23-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)
