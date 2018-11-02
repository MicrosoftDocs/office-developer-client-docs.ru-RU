---
title: Метод ConvertToString (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 747c2942478da323dfe036eb5cfe8a4bda56e45a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924703"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="7ff43-102">Метод ConvertToString (RDS)</span><span class="sxs-lookup"><span data-stu-id="7ff43-102">ConvertToString method (RDS)</span></span>


<span data-ttu-id="7ff43-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ff43-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="7ff43-104">Преобразование [набора записей](recordset-object-ado.md) MIME строку, представляющую данных набора записей.</span><span class="sxs-lookup"><span data-stu-id="7ff43-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ff43-105">Syntax</span></span>

<span data-ttu-id="7ff43-106">*DataFactory*. ConvertToString (*записей*)</span><span class="sxs-lookup"><span data-stu-id="7ff43-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7ff43-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ff43-107">Parameters</span></span>

  - <span data-ttu-id="7ff43-108">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="7ff43-108">*DataFactory*</span></span>

  - <span data-ttu-id="7ff43-109">Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff43-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="7ff43-110">*Набор записей*</span><span class="sxs-lookup"><span data-stu-id="7ff43-110">*Recordset*</span></span>

  - <span data-ttu-id="7ff43-111">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7ff43-111">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff43-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ff43-112">Remarks</span></span>

<span data-ttu-id="7ff43-113">С помощью ASP-файлы используйте **ConvertToString** внедрение **записей** в HTML-страницу, созданный на сервере для передачи его на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="7ff43-113">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="7ff43-114">**ConvertToString** сначала загружает **записей** в таблицы службы курсора и создает потока в формате MIME.</span><span class="sxs-lookup"><span data-stu-id="7ff43-114">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="7ff43-115">В клиенте удаленной службы данные можно преобразовать строку MIME обратно в полностью функциональный **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="7ff43-115">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**.</span></span> <span data-ttu-id="7ff43-116">Хорошо подходит для обработки не более 400 строк данных с не более чем 1024 байта ширину каждой строки.</span><span class="sxs-lookup"><span data-stu-id="7ff43-116">It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row.</span></span> <span data-ttu-id="7ff43-117">Вы не следует использовать для потоковой передачи данных больших двоичных ОБЪЕКТОВ и задает больших результатов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="7ff43-117">You shouldn't use it for streaming BLOB data and large result sets over HTTP.</span></span> <span data-ttu-id="7ff43-118">Без сжатия проводов выполняется в строке, очень большие наборы данных занять значительное время в транспорт по протоколу HTTP, по сравнению с формат optimized проводов tablegram определены и развернуты с удаленной службы данных его в формате собственного транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="7ff43-118">No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>


> [!NOTE]
> <span data-ttu-id="7ff43-119">При использовании страницы ASP внедрение результирующую строку MIME в HTML-страницу клиента, обратите внимание, что версии VBScript, предшествующие версии 2.0 ограничение на размер строки 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="7ff43-119">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K.</span></span> <span data-ttu-id="7ff43-120">Если это ограничение превышено, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="7ff43-120">If this limit is exceeded, an error is returned.</span></span> <span data-ttu-id="7ff43-121">Сохранение небольшого области запроса при использовании внедрение MIME с помощью ASP-файлы.</span><span class="sxs-lookup"><span data-stu-id="7ff43-121">Keep the query scope relatively small when using MIME embedding via .asp files.</span></span> <span data-ttu-id="7ff43-122">Чтобы устранить эту проблему, загрузите последнюю версию VBScript из [Центра загрузки Майкрософт](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ff43-122">To fix this, download the latest version of VBScript from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>


