---
title: Свойство Recordset.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300618"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="090a4-102">Свойство Recordset.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="090a4-102">Recordset.CacheStart property (DAO)</span></span>


<span data-ttu-id="090a4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="090a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="090a4-104">Задает или возвращает значение, которое определяет закладку первой записи в объекте Recordset типа dynaset, содержащих данные, локально кэшируемые из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="090a4-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="090a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="090a4-105">Syntax</span></span>

<span data-ttu-id="090a4-106">*выражение .* CacheStart</span><span class="sxs-lookup"><span data-stu-id="090a4-106">*expression* .CacheStart</span></span>

<span data-ttu-id="090a4-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="090a4-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="090a4-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="090a4-108">Remarks</span></span>

<span data-ttu-id="090a4-109">Кэшинг данных повышает производительность при использовании объектов **Recordset** для извлечения данных с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="090a4-109">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="090a4-110">Кэш — это пространство в локальной памяти, в которое вмещаются данные, полученные с сервера; Это полезно, если пользователи запрашивают данные еще раз во время работы приложения.</span><span class="sxs-lookup"><span data-stu-id="090a4-110">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="090a4-111">Когда пользователи запрашивают данные, ячеек базы данных Microsoft Access сначала проверяет кэш на наличие запрашиваемой информации, а не запрашивает их с сервера, что занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="090a4-111">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="090a4-112">Кэш сохраняет только данные, полученные из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="090a4-112">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="090a4-113">Любой источник данных ODBC, подключенный к ячею базы данных Microsoft Access, например связанная таблица, может иметь локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="090a4-113">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="090a4-114">Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, установите свойства **CacheSize** и **[CacheStart,](recordset-cachestart-property-dao.md)** а затем используйте метод **[FillCache](recordset-fillcache-method-dao.md)** или пошаговую обработку записей с помощью методов **Move.**</span><span class="sxs-lookup"><span data-stu-id="090a4-114">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="090a4-115">Параметр **свойства CacheStart** — это закладка первой записи в кэшированном объекте **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="090a4-115">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached.</span></span> <span data-ttu-id="090a4-116">Вы можете использовать закладку любой записи, чтобы установить **свойство CacheStart.**</span><span class="sxs-lookup"><span data-stu-id="090a4-116">You can use the bookmark of any record to set the **CacheStart** property.</span></span> <span data-ttu-id="090a4-117">Сделайте запись, которую вы хотите запустить кэш текущей записью, и установите для свойства **CacheStart** свойство **[Bookmark.](recordset-bookmark-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="090a4-117">Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="090a4-118">Механизм баз данных Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="090a4-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="090a4-119">Записи, полученные из кэша, не отражают изменения, внесенные одновременно в исходные данные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="090a4-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="090a4-120">Чтобы принудительно обновить все кэшные данные, установите для свойства **CacheSize** объекта **Recordset** 0, повторно установите для него размер кэша, который вы изначально запросили, а затем используйте метод **FillCache.**</span><span class="sxs-lookup"><span data-stu-id="090a4-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

