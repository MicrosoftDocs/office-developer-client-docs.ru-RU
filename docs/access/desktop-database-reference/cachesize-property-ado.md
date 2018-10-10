---
title: CacheSize Property (ADO)
TOCTitle: CacheSize Property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed4d104dcd6d0b90e6011a305cd3502cf671175b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482415"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="50fbf-102">CacheSize Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="50fbf-102">CacheSize Property (ADO)</span></span>


<span data-ttu-id="50fbf-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="50fbf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="50fbf-104">Указывает количество записей из объекта [набора записей](recordset-object-ado.md) , которые кэшируются локально в памяти.</span><span class="sxs-lookup"><span data-stu-id="50fbf-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="50fbf-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="50fbf-105">Settings and Return Values</span></span>

<span data-ttu-id="50fbf-106">Задает или возвращает значение типа **Long** , должно быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="50fbf-106">Sets or returns a **Long** value that must be greater than 0.</span></span> <span data-ttu-id="50fbf-107">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="50fbf-107">Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="50fbf-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="50fbf-108">Remarks</span></span>

<span data-ttu-id="50fbf-109">Используйте свойство **CacheSize** для управления количества записей для получения за один раз в локальную память от поставщика.</span><span class="sxs-lookup"><span data-stu-id="50fbf-109">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider.</span></span> <span data-ttu-id="50fbf-110">Например при **CacheSize** — 10, открыв объекта **набора записей** , поставщик получает первые 10 записей в локальную память.</span><span class="sxs-lookup"><span data-stu-id="50fbf-110">For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory.</span></span> <span data-ttu-id="50fbf-111">При переходе от объекта **набора записей** , поставщик возвращает данные из буфера локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="50fbf-111">As you move through the **Recordset** object, the provider returns the data from the local memory buffer.</span></span> <span data-ttu-id="50fbf-112">После перемещения за последние записи в кэше, поставщик извлекает следующие 10 записей из источника данных в кэш.</span><span class="sxs-lookup"><span data-stu-id="50fbf-112">As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="50fbf-113"><STRONG>CacheSize</STRONG> основано на <STRONG>Максимальное число строк Open</STRONG> поставщика свойство (в коллекции <STRONG>свойств</STRONG> объекта <STRONG>набора записей</STRONG> ).</span><span class="sxs-lookup"><span data-stu-id="50fbf-113"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object).</span></span> <span data-ttu-id="50fbf-114">Вы не может задать <STRONG>CacheSize</STRONG> значение больше, чем <STRONG>Максимальное число открытых строк</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="50fbf-114">You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>.</span></span> <span data-ttu-id="50fbf-115">Чтобы изменить число строк, которые можно открыть в поставщике, задайте <STRONG>Максимальное число открытых строк</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="50fbf-115">To modify the number of rows which can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="50fbf-116">Можно изменить значение **CacheSize** во время жизни объекта **набора записей** , но только при изменении данного значения влияет на число записей в кэше после последующих запросов из источника данных.</span><span class="sxs-lookup"><span data-stu-id="50fbf-116">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</span></span> <span data-ttu-id="50fbf-117">Изменение значения свойства сам по себе он не влияет текущего содержимого кэша.</span><span class="sxs-lookup"><span data-stu-id="50fbf-117">Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="50fbf-118">Если меньшее количество записей для извлечения чем **CacheSize** указывает, поставщик возвращает оставшихся и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="50fbf-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="50fbf-119">**CacheSize** значение 0 не допускается и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="50fbf-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="50fbf-120">Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="50fbf-120">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span> <span data-ttu-id="50fbf-121">Чтобы принудительно выполнить обновление всех кэшированных данных, используйте метод [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="50fbf-121">To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="50fbf-122">Если значение **CacheSize** больше одно навигации методы ([Перемещение](move-method-ado.md), [MoveFirst, MoveLast, MoveNext и MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) может привести к навигации для удаленной записи в случае удаления после извлечения записей.</span><span class="sxs-lookup"><span data-stu-id="50fbf-122">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="50fbf-123">После первоначальной выборки не будут отражены последующих удалений в кэше данных до попытки доступа к значение данных из удаленной строки.</span><span class="sxs-lookup"><span data-stu-id="50fbf-123">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="50fbf-124">Тем не менее указывая **CacheSize** устраняет эту проблему, поскольку удаленные строки не могут быть выбраны.</span><span class="sxs-lookup"><span data-stu-id="50fbf-124">However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

