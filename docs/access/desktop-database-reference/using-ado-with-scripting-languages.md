---
title: Using ADO with Scripting Languages
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 196366987e89f52a3c498a769fa501a3faca9dae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604437"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="edde9-102">Using ADO with Scripting Languages</span><span class="sxs-lookup"><span data-stu-id="edde9-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="edde9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="edde9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="edde9-104"><<<<<<< HEAD в среде сценариев, ADO позволяет предоставлять данные путем получения сценариев на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="edde9-104"><<<<<<< HEAD Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="edde9-105">В этом сценарии ADO, соответствующий поставщик OLE DB, который использует и других компонентов, необходимых для ссылки хранилища данных установлены на сервере под управлением Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="edde9-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="edde9-106">С помощью Active Server Pages (ASP), ADO — это компонент, указанный в скрипте, который можно создать HTML-код, например.</span><span class="sxs-lookup"><span data-stu-id="edde9-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="edde9-107">В этом HTML-содержимое может быть передан по протоколу HTTP веб-браузере клиента.</span><span class="sxs-lookup"><span data-stu-id="edde9-107">This HTML content can be passed via HTTP to a client Web browser.</span></span> <span data-ttu-id="edde9-108">Посредством использования сценариев, веб-странице можно отправить действия обратно в скрипт на сервере, что позволяет обновить, проходят через или просмотра определенных данных.</span><span class="sxs-lookup"><span data-stu-id="edde9-108">Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
<span data-ttu-id="edde9-109">=== В среде сценариев ADO позволяет предоставлять данные путем получения сценариев на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="edde9-109">======= Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="edde9-110">В этом сценарии ADO, соответствующий поставщик OLE DB, который использует и других компонентов, необходимых для ссылки хранилища данных установлены на сервере под управлением Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="edde9-110">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="edde9-111">С помощью Active Server Pages (ASP), ADO — это компонент, указанный в скрипте, который можно создать HTML-код, например.</span><span class="sxs-lookup"><span data-stu-id="edde9-111">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="edde9-112">В этом HTML-содержимое может быть передан по протоколу HTTP веб-браузере клиента.</span><span class="sxs-lookup"><span data-stu-id="edde9-112">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="edde9-113">Посредством использования сценариев, веб-страницы можно отправить действия обратно в скрипт на сервере, что позволяет обновить, проходят через или просмотра определенных данных.</span><span class="sxs-lookup"><span data-stu-id="edde9-113">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
>>>>>>> <span data-ttu-id="edde9-114">master</span><span class="sxs-lookup"><span data-stu-id="edde9-114">master</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="edde9-115">Источники данных ODBC</span><span class="sxs-lookup"><span data-stu-id="edde9-115">ODBC Data Sources</span></span>

<span data-ttu-id="edde9-116">Один важные различия между сценариев и не являющиеся скрипты кода ADO является источником данных ODBC при использовании.</span><span class="sxs-lookup"><span data-stu-id="edde9-116">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</span></span> <span data-ttu-id="edde9-117">Для приложений, не являющиеся сценариев можно создать пользовательский DSN в источники данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="edde9-117">For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</span></span> <span data-ttu-id="edde9-118">Для сценариев, работающих под управлением служб IIS необходимо создать DSN системы; в противном случае сценарии не распознает источника данных, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="edde9-118">For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created.</span></span> <span data-ttu-id="edde9-119">Это относится к любой ADO сценариев приложения с помощью поставщик Microsoft OLE DB для ODBC через Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="edde9-119">This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="edde9-120">Создание ссылок на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="edde9-120">Referencing the ADO Library</span></span>

<span data-ttu-id="edde9-121">Н/д с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="edde9-121">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="edde9-122">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="edde9-122">Handling events</span></span>

<span data-ttu-id="edde9-123">Н/д с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="edde9-123">N/A with scripting languages.</span></span>

<span data-ttu-id="edde9-124">В следующих разделах содержится более подробные сведения об использовании ADO с языками сценариев:</span><span class="sxs-lookup"><span data-stu-id="edde9-124">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="edde9-125">ADO в VBScript</span><span class="sxs-lookup"><span data-stu-id="edde9-125">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="edde9-126">ADO в JScript</span><span class="sxs-lookup"><span data-stu-id="edde9-126">ADO in JScript</span></span>](jscript-ado-programming.md)

