---
title: Свойство Recordset2.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718800"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="fa598-102">Свойство Recordset2.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa598-102">Recordset2.CacheStart property (DAO)</span></span>


<span data-ttu-id="fa598-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa598-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa598-104">Задает или возвращает значение, указывающее закладки для первой записи в объекте типа динамического набора записей, содержащий данные для локально кэшировать из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa598-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa598-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa598-105">Syntax</span></span>

<span data-ttu-id="fa598-106">*выражение* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="fa598-106">*expression* .CacheStart</span></span>

<span data-ttu-id="fa598-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="fa598-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa598-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="fa598-108">Remarks</span></span>

<span data-ttu-id="fa598-109">Кэширование данных улучшает производительность при использовании **набора записей** объектов для извлечения данных из удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa598-109">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="fa598-110">Кэш — это должен быть пробел в локальной памяти, в которой содержатся данные, недавно извлеченные с сервера. Это полезно, если пользователи запрашивать данные еще раз во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="fa598-110">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="fa598-111">Когда пользователь запрашивает данные, ядро базы данных Microsoft Access кэша для запрошенные данные сначала проверяет вместо извлечение из сервера, который занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="fa598-111">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="fa598-112">Кэш сохраняет только данные, поступающие из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="fa598-112">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="fa598-113">Любой Microsoft Access базы данных подключением модуль ODBC источник данных, например связанной таблицы может иметь локального кэша.</span><span class="sxs-lookup"><span data-stu-id="fa598-113">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="fa598-114">Создание кэша, откройте объект **набора записей** из к удаленному источнику данных, задать свойства **CacheSize** и **[CacheStart](recordset2-cachestart-property-dao.md)** и затем используйте метод **[FillCache](recordset2-fillcache-method-dao.md)** или пошаговое выполнение записи с помощью методов **перемещения** .</span><span class="sxs-lookup"><span data-stu-id="fa598-114">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="fa598-115">Значение свойства **CacheStart** — закладки для первой записи в объекте **набора записей** для кэширования.</span><span class="sxs-lookup"><span data-stu-id="fa598-115">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached.</span></span> <span data-ttu-id="fa598-116">Закладки для любой записи можно использовать для свойства **CacheStart** .</span><span class="sxs-lookup"><span data-stu-id="fa598-116">You can use the bookmark of any record to set the **CacheStart** property.</span></span> <span data-ttu-id="fa598-117">Сделать запись должна быть запущена текущей записи кэша и задайте свойство **CacheStart** свойством **[Закладка](recordset2-bookmark-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="fa598-117">Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="fa598-118">Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="fa598-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="fa598-119">Записей, полученных из кэша не отражает изменения, внесенные одновременно исходных данных другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="fa598-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="fa598-120">Чтобы принудительно выполнить обновление всех кэшированных данных, значение 0, снова задайте для него значение размера кэша, изначально запрошен, а затем использовать метод **FillCache** свойство **CacheSize** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fa598-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

