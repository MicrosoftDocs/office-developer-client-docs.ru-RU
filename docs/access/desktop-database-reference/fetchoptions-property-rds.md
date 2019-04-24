---
title: Свойство FetchOptions (RDS)
TOCTitle: FetchOptions property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd2ecf0d7d3df6d1caffd906cf318916a2a8882
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293198"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="4bcb2-102">Свойство FetchOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="4bcb2-102">FetchOptions property (RDS)</span></span>


<span data-ttu-id="4bcb2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bcb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bcb2-104">Указывает тип асинхронной загрузки.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="4bcb2-105">Значения параметров и возврата</span><span class="sxs-lookup"><span data-stu-id="4bcb2-105">Setting and Return Values</span></span>

<span data-ttu-id="4bcb2-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bcb2-107">Константа</span><span class="sxs-lookup"><span data-stu-id="4bcb2-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="4bcb2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4bcb2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bcb2-109"><strong>Адкфетчупфронт</strong></span><span class="sxs-lookup"><span data-stu-id="4bcb2-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcb2-110">Все записи объекта <a href="recordset-object-ado.md">Recordset</a> извлекаются до того, как Управление будет возвращено приложению.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-110">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application.</span></span> <span data-ttu-id="4bcb2-111">Полный <strong>набор записей</strong> извлекается до того, как приложению будет разрешено выполнять какие-либо действия.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-111">The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcb2-112"><strong>Адкфетчбаккграунд</strong></span><span class="sxs-lookup"><span data-stu-id="4bcb2-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcb2-113">Управление может вернуться к приложению, как только первый пакет записей будет извлечен.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-113">Control can return to the application as soon as the first batch of records has been fetched.</span></span> <span data-ttu-id="4bcb2-114">При последующем чтении объекта <strong>Recordset</strong> , который пытается получить доступ к записи, которая не была выбрана в первом пакете, будет задержана, пока не будет выделена запись, при которой Управление временем возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-114">A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcb2-115"><strong>Адкфетчасинк</strong></span><span class="sxs-lookup"><span data-stu-id="4bcb2-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcb2-116">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-116">Default.</span></span> <span data-ttu-id="4bcb2-117">Управление немедленно возвращается в приложение, пока записи выбираются в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-117">Control returns immediately to the application while records are fetched in the background.</span></span> <span data-ttu-id="4bcb2-118">Если приложение пытается прочитать запись, которая еще не была извлечена, будет прочитана запись, ближайшая к искомой записи, и управление будет возвращено немедленно, указывая на то, что достигнут текущий конец <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="4bcb2-118">If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached.</span></span> <span data-ttu-id="4bcb2-119">Например, при вызове <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> текущее положение текущей записи будет пересчитано на последнюю вызываемую запись, даже если дополнительные записи продолжат заполнение объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-119">For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="4bcb2-120">Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять объявления для них.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-120">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="4bcb2-121">Вы можете вырезать и вставить объявления констант из файла Адквбс. Inc, расположенного в папке C:\Program Files\Common Филес\систем\мсадк.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-121">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>



## <a name="remarks"></a><span data-ttu-id="4bcb2-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="4bcb2-122">Remarks</span></span>

<span data-ttu-id="4bcb2-123">В веб-приложении обычно требуется использовать **адкфетчасинк** (значение по умолчанию), так как оно обеспечивает лучшую производительность.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-123">In a web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="4bcb2-124">В скомпилированном клиентском приложении обычно потребуется использовать **адкфетчбаккграунд**.</span><span class="sxs-lookup"><span data-stu-id="4bcb2-124">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>

