---
title: Использование CacheSize (Справочник по базам данных Access на компьютере)
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
# <a name="using-cachesize"></a><span data-ttu-id="70418-102">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="70418-102">Using CacheSize</span></span>

<span data-ttu-id="70418-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70418-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70418-104">Используйте свойство **CacheSize** для управления количеством записей, получаемых за один раз в локальной памяти поставщика.</span><span class="sxs-lookup"><span data-stu-id="70418-104">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider.</span></span> <span data-ttu-id="70418-105">Например, если **CacheSize** имеет значение 10, после первого открытия объекта **Recordset** поставщик получает первые 10 записей в локальную память.</span><span class="sxs-lookup"><span data-stu-id="70418-105">For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory.</span></span> <span data-ttu-id="70418-106">При перемещении по объекту **Recordset** поставщик возвращает данные из буфера локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="70418-106">As you move through the **Recordset** object, the provider returns the data from the local memory buffer.</span></span> <span data-ttu-id="70418-107">Как только вы перейдете за последнюю запись в кэше, поставщик извлечет из источника данных следующие 10 записей из источника данных в кэш.</span><span class="sxs-lookup"><span data-stu-id="70418-107">As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="70418-108">**CacheSize** основано на максимальном свойстве, зависящем от поставщика **открытых строк** (в коллекции **свойств** объекта **Recordset** ).</span><span class="sxs-lookup"><span data-stu-id="70418-108">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object).</span></span> <span data-ttu-id="70418-109">Невозможно задать для **CacheSize** значение, превышающее **Максимальное число открытых строк**.</span><span class="sxs-lookup"><span data-stu-id="70418-109">You cannot set **CacheSize** to a value greater than **Maximum Open Rows**.</span></span> <span data-ttu-id="70418-110">Чтобы изменить количество строк, которые может открыть поставщик, установите **Максимальное число открытых строк**.</span><span class="sxs-lookup"><span data-stu-id="70418-110">To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="70418-111">Значение **CacheSize** может быть скорректировано в течение всего времени существования объекта **Recordset** , но изменение этого значения влияет только на число записей в кэше после последующих извлечений из источника данных.</span><span class="sxs-lookup"><span data-stu-id="70418-111">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</span></span> <span data-ttu-id="70418-112">Изменение только значения свойства не приводит к изменению текущего содержимого кэша.</span><span class="sxs-lookup"><span data-stu-id="70418-112">Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="70418-113">Если количество записей для получения меньше, чем **CacheSize** , поставщик возвращает оставшиеся записи, и ошибка не возникнет.</span><span class="sxs-lookup"><span data-stu-id="70418-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="70418-114">Нулевое значение параметра **CacheSize** не допускается и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="70418-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="70418-115">Записи, извлеченные из кэша, не отражают параллельные изменения, внесенные другими пользователями в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="70418-115">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data.</span></span> <span data-ttu-id="70418-116">Чтобы принудительно обновить все кэшированные данные, используйте метод [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70418-116">To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="70418-117">Если для **CacheSize** задано значение больше 1, методы навигации ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext и MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) могут привести к переходу на удаленную запись, если удаление происходит после извлечения записей.</span><span class="sxs-lookup"><span data-stu-id="70418-117">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="70418-118">После первоначальной загрузки последующие удаления не будут отражены в кэше данных до тех пор, пока вы не попытаетесь получить доступ к значению данных из удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="70418-118">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="70418-119">Однако установка **CacheSize** в 1 исключает эту ошибку, так как не удается извлечь удаленные строки.</span><span class="sxs-lookup"><span data-stu-id="70418-119">However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

