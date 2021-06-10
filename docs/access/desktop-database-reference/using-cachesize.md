---
title: Использование CacheSize (Ссылка на настольные базы данных)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312126"
---
# <a name="using-cachesize"></a><span data-ttu-id="837d6-102">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="837d6-102">Using CacheSize</span></span>

<span data-ttu-id="837d6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="837d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="837d6-104">Используйте **свойство CacheSize** для управления количеством записей, которые можно получить одновременно в локальной памяти поставщика.</span><span class="sxs-lookup"><span data-stu-id="837d6-104">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider.</span></span> <span data-ttu-id="837d6-105">Например, если **CacheSize** — 10, после первого открытия объекта **Recordset** поставщик извлекает первые 10 записей в локализованную память.</span><span class="sxs-lookup"><span data-stu-id="837d6-105">For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory.</span></span> <span data-ttu-id="837d6-106">При переходе через **объект Recordset** поставщик возвращает данные из локального буфера памяти.</span><span class="sxs-lookup"><span data-stu-id="837d6-106">As you move through the **Recordset** object, the provider returns the data from the local memory buffer.</span></span> <span data-ttu-id="837d6-107">После перемещения последней записи в кэше поставщик извлекает следующие 10 записей из источника данных в кэш.</span><span class="sxs-lookup"><span data-stu-id="837d6-107">As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="837d6-108">**CacheSize** основан на свойстве **поставщика Maximum Open Rows** (в коллекции **Свойств** объекта **Recordset).**</span><span class="sxs-lookup"><span data-stu-id="837d6-108">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object).</span></span> <span data-ttu-id="837d6-109">Невозможно установить **значение CacheSize,** большее, чем **максимально открытые строки.**</span><span class="sxs-lookup"><span data-stu-id="837d6-109">You cannot set **CacheSize** to a value greater than **Maximum Open Rows**.</span></span> <span data-ttu-id="837d6-110">Чтобы изменить количество строк, которые может открыть поставщик, установите **максимальные открытые строки.**</span><span class="sxs-lookup"><span data-stu-id="837d6-110">To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="837d6-111">Значение **CacheSize** может быть скорректировано в течение жизни объекта **Recordset,** но изменение этого значения влияет только на количество записей в кэше после последующих искавалов из источника данных.</span><span class="sxs-lookup"><span data-stu-id="837d6-111">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</span></span> <span data-ttu-id="837d6-112">Только изменение значения свойства не изменит текущее содержимое кэша.</span><span class="sxs-lookup"><span data-stu-id="837d6-112">Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="837d6-113">Если записей для получения меньше, чем указывает **CacheSize,** поставщик возвращает оставшиеся записи, и ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="837d6-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="837d6-114">Параметр **CacheSize** с нолем не допускается и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="837d6-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="837d6-115">Записи, извлеченные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="837d6-115">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data.</span></span> <span data-ttu-id="837d6-116">Для принудительного обновления всех кэшных данных используйте [метод Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="837d6-116">To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="837d6-117">Если **значение CacheSize** превышает 1, методы навигации [(Move,](move-method-ado.md) [MoveFirst, MoveLast, MoveNext и MovePrevious)](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)могут привести к переходу на удаленную запись, если удаление происходит после получения записей.</span><span class="sxs-lookup"><span data-stu-id="837d6-117">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="837d6-118">После первоначального получения последующие удаления не будут отражаться в кэше данных, пока вы не попытайтесь получить доступ к значению данных из удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="837d6-118">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="837d6-119">Однако параметр **CacheSize** до 1 устраняет эту проблему, так как удаленные строки не могут быть извлечены.</span><span class="sxs-lookup"><span data-stu-id="837d6-119">However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

