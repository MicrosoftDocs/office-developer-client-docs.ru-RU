---
title: Свойство FetchOptions (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b018fda52ba7dd311cda9b7b23ce10d5e47c4828
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868932"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="3b4e9-102">Свойство FetchOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="3b4e9-102">FetchOptions Property (RDS)</span></span>


<span data-ttu-id="3b4e9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b4e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b4e9-104">Указывает тип асинхронной выборки.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="3b4e9-105">Задание и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3b4e9-105">Setting and Return Values</span></span>

<span data-ttu-id="3b4e9-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b4e9-107">Константа</span><span class="sxs-lookup"><span data-stu-id="3b4e9-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="3b4e9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3b4e9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b4e9-109"><strong>adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="3b4e9-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="3b4e9-110">Все записи из <a href="recordset-object-ado.md">набора записей</a> будут выбраны до возврата управления к приложению.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-110">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application.</span></span> <span data-ttu-id="3b4e9-111">Полный <strong>набор записей</strong> извлекается перед приложение может выполнять любые действия с ним.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-111">The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b4e9-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="3b4e9-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="3b4e9-113">Элемент управления может вернуть приложению сразу после первого пакета записей будут выбраны.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-113">Control can return to the application as soon as the first batch of records has been fetched.</span></span> <span data-ttu-id="3b4e9-114">Последующие чтение <strong>записей</strong> , что будет отложено попытки доступа к записи, не извлечь в первого пакета, пока искомому запись фактически выбраны, в какой момент элемент управления возвращает приложению.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-114">A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b4e9-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="3b4e9-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="3b4e9-116">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-116">Default.</span></span> <span data-ttu-id="3b4e9-117">Управление немедленно возвращается приложению во время записи получены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-117">Control returns immediately to the application while records are fetched in the background.</span></span> <span data-ttu-id="3b4e9-118">Если приложение пытается считать запись, которая еще не выбраны, наиболее близкого к искомому запись запись будет считывать и элемент управления будет возвращать немедленно, указывающего на то, что достигнут конец текущего <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3b4e9-118">If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached.</span></span> <span data-ttu-id="3b4e9-119">К примеру вызов <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> будут перемещаться положения текущей записи последней записи фактически извлечь несмотря на то, что будет предоставляться несколько записей для заполнения <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-119">For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="3b4e9-120">Каждый исполняемый файл со стороны клиента, который использует эти константы необходимо предоставить объявления для них.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-120">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="3b4e9-121">Можно вырежьте и вставьте объявлений констант из файла Adcvbs.inc, находящийся в папке C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-121">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>



## <a name="remarks"></a><span data-ttu-id="3b4e9-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b4e9-122">Remarks</span></span>

<span data-ttu-id="3b4e9-123">В веб-приложении обычно требуется использовать **adcFetchAsync** (значение по умолчанию), так как он обеспечивает более высокую производительность.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-123">In a web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="3b4e9-124">В скомпилированном клиентское приложение, которое обычно требуется использовать **adcFetchBackground**.</span><span class="sxs-lookup"><span data-stu-id="3b4e9-124">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>

