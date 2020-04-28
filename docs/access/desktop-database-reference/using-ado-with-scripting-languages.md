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
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="b2a35-102">Использование ADO со скриптовыми языками</span><span class="sxs-lookup"><span data-stu-id="b2a35-102">Using ADO with scripting languages</span></span>


<span data-ttu-id="b2a35-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2a35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2a35-104">В среде сценариев ADO позволяет предоставлять данные с помощью серверных скриптов.</span><span class="sxs-lookup"><span data-stu-id="b2a35-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="b2a35-105">В этом сценарии ADO, используемый поставщик OLE DB, который он использует, и все остальные компоненты, необходимые для ссылки на данное хранилище данных, устанавливаются на сервер, на котором выполняются службы IIS.</span><span class="sxs-lookup"><span data-stu-id="b2a35-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="b2a35-106">С помощью ASP (Active Server Pages) ADO является компонентом, на который ссылается скрипт, который может создавать HTML, например.</span><span class="sxs-lookup"><span data-stu-id="b2a35-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="b2a35-107">Это содержимое HTML может передаваться через HTTP в клиентский веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="b2a35-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="b2a35-108">С помощью сценариев веб-страница может отправлять действия обратно на серверный сценарий, позволяя обновлять, просматривать и просматривать определенные данные.</span><span class="sxs-lookup"><span data-stu-id="b2a35-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="b2a35-109">Источники данных ODBC</span><span class="sxs-lookup"><span data-stu-id="b2a35-109">ODBC Data Sources</span></span>

<span data-ttu-id="b2a35-110">Важным различием между сценариями и кода ADO без написания скриптов является источник данных ODBC, если он используется.</span><span class="sxs-lookup"><span data-stu-id="b2a35-110">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</span></span> <span data-ttu-id="b2a35-111">Для приложений, не использующих сценарии, можно создать пользовательское имя DSN в администраторе источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="b2a35-111">For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</span></span> <span data-ttu-id="b2a35-112">Для сценариев, выполняемых в службах IIS, необходимо создать системный DSN. в противном случае ваши скрипты не смогут распознать созданный вами источник данных.</span><span class="sxs-lookup"><span data-stu-id="b2a35-112">For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created.</span></span> <span data-ttu-id="b2a35-113">Это относится ко всем приложениям сценариев ADO с помощью поставщика Microsoft OLE DB для ODBC через Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="b2a35-113">This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="b2a35-114">Создание ссылок на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="b2a35-114">Referencing the ADO Library</span></span>

<span data-ttu-id="b2a35-115">N/A с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="b2a35-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="b2a35-116">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="b2a35-116">Handling events</span></span>

<span data-ttu-id="b2a35-117">N/A с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="b2a35-117">N/A with scripting languages.</span></span>

<span data-ttu-id="b2a35-118">В следующих разделах содержатся более конкретные сведения об использовании ADO с языками сценариев:</span><span class="sxs-lookup"><span data-stu-id="b2a35-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="b2a35-119">JScript ADO Programming</span><span class="sxs-lookup"><span data-stu-id="b2a35-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="b2a35-120">VBScript ADO Programming</span><span class="sxs-lookup"><span data-stu-id="b2a35-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)
