---
title: Использование ADO со скриптовыми языками
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d357fe07a93548419fd03745541435d94d59a8c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861038"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="5c5bb-102">Использование ADO со скриптовыми языками</span><span class="sxs-lookup"><span data-stu-id="5c5bb-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="5c5bb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c5bb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c5bb-104"><<<<<<< HEAD в среде сценариев, ADO позволяет предоставлять данные путем получения сценариев на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-104"><<<<<<< HEAD Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="5c5bb-105">В этом сценарии ADO, соответствующий поставщик OLE DB, который использует и других компонентов, необходимых для ссылки хранилища данных установлены на сервере под управлением Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="5c5bb-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="5c5bb-106">С помощью Active Server Pages (ASP), ADO — это компонент, указанный в скрипте, который можно создать HTML-код, например.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="5c5bb-107">В этом HTML-содержимое может быть передан по протоколу HTTP веб-браузере клиента.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-107">This HTML content can be passed via HTTP to a client Web browser.</span></span> <span data-ttu-id="5c5bb-108">Посредством использования сценариев, веб-странице можно отправить действия обратно в скрипт на сервере, что позволяет обновить, проходят через или просмотра определенных данных.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-108">Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
<span data-ttu-id="5c5bb-109">=== В среде сценариев ADO позволяет предоставлять данные путем получения сценариев на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-109">======= Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="5c5bb-110">В этом сценарии ADO, соответствующий поставщик OLE DB, который использует и других компонентов, необходимых для ссылки хранилища данных установлены на сервере под управлением Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="5c5bb-110">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="5c5bb-111">С помощью Active Server Pages (ASP), ADO — это компонент, указанный в скрипте, который можно создать HTML-код, например.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-111">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="5c5bb-112">В этом HTML-содержимое может быть передан по протоколу HTTP веб-браузере клиента.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-112">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="5c5bb-113">Посредством использования сценариев, веб-страницы можно отправить действия обратно в скрипт на сервере, что позволяет обновить, проходят через или просмотра определенных данных.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-113">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
>>>>>>> <span data-ttu-id="5c5bb-114">образец</span><span class="sxs-lookup"><span data-stu-id="5c5bb-114">master</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="5c5bb-115">Источники данных ODBC</span><span class="sxs-lookup"><span data-stu-id="5c5bb-115">ODBC Data Sources</span></span>

<span data-ttu-id="5c5bb-116">Один важные различия между сценариев и не являющиеся скрипты кода ADO является источником данных ODBC при использовании.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-116">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</span></span> <span data-ttu-id="5c5bb-117">Для приложений, не являющиеся сценариев можно создать пользовательский DSN в источники данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-117">For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</span></span> <span data-ttu-id="5c5bb-118">Для сценариев, работающих под управлением служб IIS необходимо создать DSN системы; в противном случае сценарии не распознает источника данных, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-118">For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created.</span></span> <span data-ttu-id="5c5bb-119">Это относится к любой ADO сценариев приложения с помощью поставщик Microsoft OLE DB для ODBC через Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-119">This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="5c5bb-120">Создание ссылок на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="5c5bb-120">Referencing the ADO Library</span></span>

<span data-ttu-id="5c5bb-121">Н/д с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-121">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="5c5bb-122">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="5c5bb-122">Handling events</span></span>

<span data-ttu-id="5c5bb-123">Н/д с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="5c5bb-123">N/A with scripting languages.</span></span>

<span data-ttu-id="5c5bb-124">В следующих разделах содержится более подробные сведения об использовании ADO с языками сценариев:</span><span class="sxs-lookup"><span data-stu-id="5c5bb-124">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="5c5bb-125">Программирование для ADO на JScript</span><span class="sxs-lookup"><span data-stu-id="5c5bb-125">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="5c5bb-126">Программирование для ADO на VBScript</span><span class="sxs-lookup"><span data-stu-id="5c5bb-126">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)