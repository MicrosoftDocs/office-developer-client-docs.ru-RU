---
title: Использование ADO со скриптовыми языками
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00854a56428a99a4d033f7959690836f88912c77
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944804"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="97fc7-102">С помощью ADO с языками сценариев</span><span class="sxs-lookup"><span data-stu-id="97fc7-102">Using ADO with scripting languages</span></span>


<span data-ttu-id="97fc7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97fc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97fc7-104">В среде сценариев ADO позволяет предоставлять данные путем получения сценариев на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="97fc7-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="97fc7-105">В этом сценарии ADO, соответствующий поставщик OLE DB, который использует и других компонентов, необходимых для ссылки хранилища данных установлены на сервере под управлением Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="97fc7-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="97fc7-106">С помощью Active Server Pages (ASP), ADO — это компонент, указанный в скрипте, который можно создать HTML-код, например.</span><span class="sxs-lookup"><span data-stu-id="97fc7-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="97fc7-107">В этом HTML-содержимое может быть передан по протоколу HTTP веб-браузере клиента.</span><span class="sxs-lookup"><span data-stu-id="97fc7-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="97fc7-108">Посредством использования сценариев, веб-страницы можно отправить действия обратно в скрипт на сервере, что позволяет обновить, проходят через или просмотра определенных данных.</span><span class="sxs-lookup"><span data-stu-id="97fc7-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="97fc7-109">Источники данных ODBC</span><span class="sxs-lookup"><span data-stu-id="97fc7-109">ODBC Data Sources</span></span>

<span data-ttu-id="97fc7-110">Один важные различия между сценариев и не являющиеся скрипты кода ADO является источником данных ODBC при использовании.</span><span class="sxs-lookup"><span data-stu-id="97fc7-110">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</span></span> <span data-ttu-id="97fc7-111">Для приложений, не являющиеся сценариев можно создать пользовательский DSN в источники данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="97fc7-111">For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</span></span> <span data-ttu-id="97fc7-112">Для сценариев, работающих под управлением служб IIS необходимо создать DSN системы; в противном случае сценарии не распознает источника данных, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="97fc7-112">For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created.</span></span> <span data-ttu-id="97fc7-113">Это относится к любой ADO сценариев приложения с помощью поставщик Microsoft OLE DB для ODBC через Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="97fc7-113">This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="97fc7-114">Создание ссылок на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="97fc7-114">Referencing the ADO Library</span></span>

<span data-ttu-id="97fc7-115">Н/д с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="97fc7-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="97fc7-116">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="97fc7-116">Handling events</span></span>

<span data-ttu-id="97fc7-117">Н/д с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="97fc7-117">N/A with scripting languages.</span></span>

<span data-ttu-id="97fc7-118">В следующих разделах содержится более подробные сведения об использовании ADO с языками сценариев:</span><span class="sxs-lookup"><span data-stu-id="97fc7-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="97fc7-119">Программирование для ADO на JScript</span><span class="sxs-lookup"><span data-stu-id="97fc7-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="97fc7-120">Программирование для ADO на VBScript</span><span class="sxs-lookup"><span data-stu-id="97fc7-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)