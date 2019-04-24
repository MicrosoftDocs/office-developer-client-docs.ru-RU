---
title: Метод ConvertToString (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2c589339eb838f944ce4443c19a787eafb01c3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295515"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="2748a-102">Метод ConvertToString (RDS)</span><span class="sxs-lookup"><span data-stu-id="2748a-102">ConvertToString method (RDS)</span></span>

<span data-ttu-id="2748a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2748a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="2748a-104">Преобразует объект [Recordset](recordset-object-ado.md) в строку MIME, представляющую данные набора записей.</span><span class="sxs-lookup"><span data-stu-id="2748a-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2748a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2748a-105">Syntax</span></span>

<span data-ttu-id="2748a-106">*Фактическое*. ConvertToString (*Recordset*)</span><span class="sxs-lookup"><span data-stu-id="2748a-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2748a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2748a-107">Parameters</span></span>

|<span data-ttu-id="2748a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2748a-108">Parameter</span></span>|<span data-ttu-id="2748a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2748a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2748a-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="2748a-110">*DataFactory*</span></span> |<span data-ttu-id="2748a-111">Объектная переменная, представляющая объект [фактОв рдссервер.](datafactory-object-rdsserver.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="2748a-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="2748a-112">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="2748a-112">*Recordset*</span></span> |<span data-ttu-id="2748a-113">Объектная переменная, представляющая объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2748a-113">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2748a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2748a-114">Remarks</span></span>

<span data-ttu-id="2748a-115">С помощью файлов. ASP используйте **ConvertToString** , чтобы внедрить **набор записей** на HTML-страницу, созданную на сервере, чтобы передать его на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="2748a-115">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="2748a-116">**ConvertToString** сначала загружает **набор записей** в таблицы службы курсоров, а затем создает поток в формате MIME.</span><span class="sxs-lookup"><span data-stu-id="2748a-116">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="2748a-117">На клиенте служба удаленных данных может преобразовать строку MIME обратно в полностью работоспособный **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="2748a-117">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**.</span></span> <span data-ttu-id="2748a-118">Он подходит для обработки менее 400 строк данных, размер которых не превышает 1024 байт в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="2748a-118">It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row.</span></span> <span data-ttu-id="2748a-119">Его не следует использовать для потоковой передачи больших ДВОИЧных данных и больших наборов результатов по ПРОТОКОЛу HTTP.</span><span class="sxs-lookup"><span data-stu-id="2748a-119">You shouldn't use it for streaming BLOB data and large result sets over HTTP.</span></span> <span data-ttu-id="2748a-120">В строке не выполняется сжатие по каналу, поэтому очень большие наборы данных потребуют значительного времени для транспорта по ПРОТОКОЛу HTTP, по сравнению с форматом таблеграм, определенным и развернутым удаленной службой данных в качестве собственного формата транспортного протокола.</span><span class="sxs-lookup"><span data-stu-id="2748a-120">No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>

> [!NOTE]
> <span data-ttu-id="2748a-121">Если вы используете страницы Active Server для внедрения полученной строки MIME на клиентской HTML-странице, имейте в виду, что более ранние версии VBScript, чем версия 2,0, ограничивают размер строки до 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="2748a-121">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K.</span></span> <span data-ttu-id="2748a-122">Если это ограничение превышено, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="2748a-122">If this limit is exceeded, an error is returned.</span></span> <span data-ttu-id="2748a-123">При внедрении MIME с помощью файлов ASP отДерживайте область запроса относительно небольшой.</span><span class="sxs-lookup"><span data-stu-id="2748a-123">Keep the query scope relatively small when using MIME embedding via .asp files.</span></span> <span data-ttu-id="2748a-124">Чтобы устранить эту проблему, скачайте последнюю версию VBScript из [центра загрузки Майкрософт](https://www.microsoft.com/download/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="2748a-124">To fix this, download the latest version of VBScript from the [Microsoft Download Center](https://www.microsoft.com/download/default.aspx).</span></span>


