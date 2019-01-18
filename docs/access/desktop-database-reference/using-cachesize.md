---
title: С помощью CacheSize (Справочник по для настольных баз данных Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718961"
---
# <a name="using-cachesize"></a><span data-ttu-id="ba1db-102">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="ba1db-102">Using CacheSize</span></span>

<span data-ttu-id="ba1db-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba1db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba1db-104">Используйте свойство **CacheSize** для управления количества записей для получения за один раз в локальную память от поставщика.</span><span class="sxs-lookup"><span data-stu-id="ba1db-104">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider.</span></span> <span data-ttu-id="ba1db-105">Например при **CacheSize** — 10, открыв объекта **набора записей** , поставщик получает первые 10 записей в локальную память.</span><span class="sxs-lookup"><span data-stu-id="ba1db-105">For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory.</span></span> <span data-ttu-id="ba1db-106">При переходе от объекта **набора записей** , поставщик возвращает данные из буфера локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="ba1db-106">As you move through the **Recordset** object, the provider returns the data from the local memory buffer.</span></span> <span data-ttu-id="ba1db-107">После перемещения за последние записи в кэше, поставщик извлекает следующие 10 записей из источника данных в кэш.</span><span class="sxs-lookup"><span data-stu-id="ba1db-107">As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="ba1db-108">**CacheSize** основано на **Максимальное число строк Open** поставщика свойство (в коллекции **свойств** объекта **набора записей** ).</span><span class="sxs-lookup"><span data-stu-id="ba1db-108">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object).</span></span> <span data-ttu-id="ba1db-109">Вы не может задать **CacheSize** значение больше, чем **Максимальное число открытых строк**.</span><span class="sxs-lookup"><span data-stu-id="ba1db-109">You cannot set **CacheSize** to a value greater than **Maximum Open Rows**.</span></span> <span data-ttu-id="ba1db-110">Чтобы изменить число строк, которые могут быть открыты поставщиком, задайте **Максимальное число открытых строк**.</span><span class="sxs-lookup"><span data-stu-id="ba1db-110">To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="ba1db-111">Можно изменить значение **CacheSize** во время жизни объекта **набора записей** , но только при изменении данного значения влияет на число записей в кэше после последующих запросов из источника данных.</span><span class="sxs-lookup"><span data-stu-id="ba1db-111">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</span></span> <span data-ttu-id="ba1db-112">Изменение значения свойства сам по себе он не влияет текущего содержимого кэша.</span><span class="sxs-lookup"><span data-stu-id="ba1db-112">Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="ba1db-113">Если меньшее количество записей для извлечения чем **CacheSize** указывает, поставщик возвращает оставшихся и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="ba1db-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="ba1db-114">**CacheSize** значение 0 не допускается и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ba1db-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="ba1db-115">Записей, полученных из кэша отражают параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="ba1db-115">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data.</span></span> <span data-ttu-id="ba1db-116">Чтобы принудительно выполнить обновление всех кэшированных данных, используйте метод [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1db-116">To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="ba1db-117">Если **CacheSize** присвоено значение больше 1, в случае удаления после записи были извлечены методы навигации ([Перемещение](move-method-ado.md), [MoveFirst, MoveLast, MoveNext и MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) может привести навигации для удаленной записи.</span><span class="sxs-lookup"><span data-stu-id="ba1db-117">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="ba1db-118">После первоначальной выборки не будут отражены последующих удалений в кэше данных до попытки доступа к значение данных из удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="ba1db-118">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="ba1db-119">Тем не менее установки для параметра 1 **CacheSize** устраняет эту проблему, так как удаленные строки не могут быть выбраны.</span><span class="sxs-lookup"><span data-stu-id="ba1db-119">However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

