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
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="24757-102">Свойство FetchOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="24757-102">FetchOptions property (RDS)</span></span>


<span data-ttu-id="24757-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24757-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24757-104">Указывает тип асинхронного извлечения.</span><span class="sxs-lookup"><span data-stu-id="24757-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="24757-105">Установка и возврат значений</span><span class="sxs-lookup"><span data-stu-id="24757-105">Setting and Return Values</span></span>

<span data-ttu-id="24757-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="24757-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24757-107">Константа</span><span class="sxs-lookup"><span data-stu-id="24757-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="24757-108">Описание</span><span class="sxs-lookup"><span data-stu-id="24757-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24757-109"><strong>adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="24757-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="24757-110">Все записи <a href="recordset-object-ado.md">recordset</a> извлекаются перед возвратом управления в приложение.</span><span class="sxs-lookup"><span data-stu-id="24757-110">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application.</span></span> <span data-ttu-id="24757-111">Полный набор <strong>записей получается</strong> до того, как приложению будет разрешено что-либо делать с ним.</span><span class="sxs-lookup"><span data-stu-id="24757-111">The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24757-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="24757-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="24757-113">Управление может возвращаться в приложение сразу после получения первого пакета записей.</span><span class="sxs-lookup"><span data-stu-id="24757-113">Control can return to the application as soon as the first batch of records has been fetched.</span></span> <span data-ttu-id="24757-114">Последующее чтение <strong></strong> наборов записей, пытающаяся получить доступ к записи, не извлеченной в первом пакете, будет отложена до тех пор, пока не будет фактически извлечена искомая запись, после чего контроль времени возвращается в приложение.</span><span class="sxs-lookup"><span data-stu-id="24757-114">A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24757-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="24757-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="24757-116">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24757-116">Default.</span></span> <span data-ttu-id="24757-117">При извлечении записей в фоновом режиме управление немедленно возвращается в приложение.</span><span class="sxs-lookup"><span data-stu-id="24757-117">Control returns immediately to the application while records are fetched in the background.</span></span> <span data-ttu-id="24757-118">Если приложение пытается прочитать еще не извлеченную запись, запись, ближе всего к искомой записи, будет прочитана, а управление будет возвращено немедленно, что указывает на то, что текущий конец <strong>recordset</strong> был достигнут.</span><span class="sxs-lookup"><span data-stu-id="24757-118">If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached.</span></span> <span data-ttu-id="24757-119">Например, вызов <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> переместит текущую позицию записи в последнюю фактически извлеченную запись, несмотря на то что другие записи продолжат заполнять <strong>набор записей.</strong></span><span class="sxs-lookup"><span data-stu-id="24757-119">For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="24757-120">Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять для них объявления.</span><span class="sxs-lookup"><span data-stu-id="24757-120">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="24757-121">Вы можете вырезать и ввести нужные объявления констант из файла Adcvbs.inc, расположенного в папке C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="24757-121">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>



## <a name="remarks"></a><span data-ttu-id="24757-122">Заметки</span><span class="sxs-lookup"><span data-stu-id="24757-122">Remarks</span></span>

<span data-ttu-id="24757-123">В веб-приложении обычно необходимо использовать **adcFetchAsync** (значение по умолчанию), так как оно обеспечивает лучшую производительность.</span><span class="sxs-lookup"><span data-stu-id="24757-123">In a web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="24757-124">В скомпилном клиентском приложении обычно необходимо использовать **adcFetchBackground.**</span><span class="sxs-lookup"><span data-stu-id="24757-124">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>

