---
title: ConvertToString Method (RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa1a4326cf318a9cbcddf8ebcdf584543ac8ebfb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482527"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="1dd33-102">ConvertToString Method (RDS)</span><span class="sxs-lookup"><span data-stu-id="1dd33-102">ConvertToString Method (RDS)</span></span>


<span data-ttu-id="1dd33-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1dd33-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="1dd33-104">Преобразование [набора записей](recordset-object-ado.md) MIME строку, представляющую данных набора записей.</span><span class="sxs-lookup"><span data-stu-id="1dd33-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd33-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dd33-105">Syntax</span></span>

<span data-ttu-id="1dd33-106">*DataFactory*. ConvertToString (*записей*)</span><span class="sxs-lookup"><span data-stu-id="1dd33-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="1dd33-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dd33-107">Parameters</span></span>

  - <span data-ttu-id="1dd33-108">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="1dd33-108">*DataFactory*</span></span>

  - <span data-ttu-id="1dd33-109">Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1dd33-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="1dd33-110">*Набор записей*</span><span class="sxs-lookup"><span data-stu-id="1dd33-110">*Recordset*</span></span>

  - <span data-ttu-id="1dd33-111">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1dd33-111">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd33-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="1dd33-112">Remarks</span></span>

<span data-ttu-id="1dd33-113">С помощью ASP-файлы используйте **ConvertToString** внедрение **записей** в HTML-страницу, созданный на сервере для передачи его на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="1dd33-113">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="1dd33-114">**ConvertToString** сначала загружает **записей** в таблицы службы курсора и создает потока в формате MIME.</span><span class="sxs-lookup"><span data-stu-id="1dd33-114">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="1dd33-115">В клиенте удаленной службы данные можно преобразовать строку MIME обратно в полностью функциональный **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="1dd33-115">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**.</span></span> <span data-ttu-id="1dd33-116">Хорошо подходит для обработки не более 400 строк данных с не более чем 1024 байта ширину каждой строки.</span><span class="sxs-lookup"><span data-stu-id="1dd33-116">It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row.</span></span> <span data-ttu-id="1dd33-117">Вы не следует использовать для потоковой передачи данных больших двоичных ОБЪЕКТОВ и задает больших результатов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="1dd33-117">You shouldn't use it for streaming BLOB data and large result sets over HTTP.</span></span> <span data-ttu-id="1dd33-118">Без сжатия проводов выполняется в строке, очень большие наборы данных занять значительное время в транспорт по протоколу HTTP, по сравнению с формат optimized проводов tablegram определены и развернуты с удаленной службы данных его в формате собственного транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="1dd33-118">No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1dd33-119">При использовании страницы ASP внедрение результирующую строку MIME в HTML-страницу клиента, обратите внимание, что версии VBScript, предшествующие версии 2.0 ограничение на размер строки 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="1dd33-119">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K.</span></span> <span data-ttu-id="1dd33-120">Если это ограничение превышено, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="1dd33-120">If this limit is exceeded, an error is returned.</span></span> <span data-ttu-id="1dd33-121">Сохранение небольшого области запроса при использовании внедрение MIME с помощью ASP-файлы.</span><span class="sxs-lookup"><span data-stu-id="1dd33-121">Keep the query scope relatively small when using MIME embedding via .asp files.</span></span> <span data-ttu-id="1dd33-122">Чтобы устранить эту проблему, загрузите последнюю версию VBScript из <A href="https://www.microsoft.com/downloads/en/default.aspx">Центра загрузки Майкрософт</A>.</span><span class="sxs-lookup"><span data-stu-id="1dd33-122">To fix this, download the latest version of VBScript from the <A href="https://www.microsoft.com/downloads/en/default.aspx">Microsoft Download Center</A>.</span></span></P>


