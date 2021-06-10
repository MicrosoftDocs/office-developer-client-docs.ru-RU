---
title: Свойство CacheSize (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 725c2f81b3f3bce05a3007c50705e9cf35f7008f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296747"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="c784a-102">Свойство CacheSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="c784a-102">CacheSize property (ADO)</span></span>


<span data-ttu-id="c784a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c784a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c784a-104">Указывает количество записей из объекта [Recordset,](recordset-object-ado.md) кэшироваться локально в памяти.</span><span class="sxs-lookup"><span data-stu-id="c784a-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c784a-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="c784a-105">Settings and return values</span></span>

<span data-ttu-id="c784a-106">Задает или возвращает значение **Long,** которое должно быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="c784a-106">Sets or returns a **Long** value that must be greater than 0.</span></span> <span data-ttu-id="c784a-107">Значение по умолчанию  1.</span><span class="sxs-lookup"><span data-stu-id="c784a-107">Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="c784a-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c784a-108">Remarks</span></span>

<span data-ttu-id="c784a-109">Используйте **свойство CacheSize** для управления количеством записей, которые можно получить одновременно в локальной памяти поставщика.</span><span class="sxs-lookup"><span data-stu-id="c784a-109">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider.</span></span> <span data-ttu-id="c784a-110">Например, если **CacheSize** — 10, после первого открытия объекта **Recordset** поставщик извлекает первые 10 записей в локализованную память.</span><span class="sxs-lookup"><span data-stu-id="c784a-110">For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory.</span></span> <span data-ttu-id="c784a-111">При переходе через **объект Recordset** поставщик возвращает данные из локального буфера памяти.</span><span class="sxs-lookup"><span data-stu-id="c784a-111">As you move through the **Recordset** object, the provider returns the data from the local memory buffer.</span></span> <span data-ttu-id="c784a-112">После перемещения последней записи в кэше поставщик извлекает следующие 10 записей из источника данных в кэш.</span><span class="sxs-lookup"><span data-stu-id="c784a-112">As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="c784a-113">**CacheSize** основан на свойстве **поставщика Maximum Open Rows** (в коллекции **Свойств** объекта **Recordset).**</span><span class="sxs-lookup"><span data-stu-id="c784a-113">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object).</span></span> <span data-ttu-id="c784a-114">Невозможно установить **значение CacheSize,** большее, чем **максимально открытые строки.**</span><span class="sxs-lookup"><span data-stu-id="c784a-114">You cannot set **CacheSize** to a value greater than **Maximum Open Rows**.</span></span> <span data-ttu-id="c784a-115">Чтобы изменить количество строк, которые может открыть поставщик, установите **максимальные открытые строки.**</span><span class="sxs-lookup"><span data-stu-id="c784a-115">To modify the number of rows which can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="c784a-116">Значение **CacheSize** может быть скорректировано в течение жизни объекта **Recordset,** но изменение этого значения влияет только на количество записей в кэше после последующих искавалов из источника данных.</span><span class="sxs-lookup"><span data-stu-id="c784a-116">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</span></span> <span data-ttu-id="c784a-117">Только изменение значения свойства не изменит текущее содержимое кэша.</span><span class="sxs-lookup"><span data-stu-id="c784a-117">Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="c784a-118">Если записей для получения меньше, чем указывает **CacheSize,** поставщик возвращает оставшиеся записи, и ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="c784a-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="c784a-119">Параметр **CacheSize** с нолем не допускается и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c784a-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="c784a-120">Записи, извлеченные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="c784a-120">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span> <span data-ttu-id="c784a-121">Для принудительного обновления всех кэшных данных используйте [метод Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c784a-121">To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="c784a-122">Если **значение CacheSize** превышает одно, методы навигации [(Move,](move-method-ado.md) [MoveFirst, MoveLast, MoveNext и MovePrevious)](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)могут привести к переходу на удаленную запись, если удаление происходит после получения записей.</span><span class="sxs-lookup"><span data-stu-id="c784a-122">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="c784a-123">После первоначального получения последующие удаления не будут отражаться в кэше данных, пока вы не попытайтесь получить доступ к значению данных из удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="c784a-123">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="c784a-124">Однако настройка **CacheSize** для одного устраняет эту проблему, так как удаленные строки не могут быть извлечены.</span><span class="sxs-lookup"><span data-stu-id="c784a-124">However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

