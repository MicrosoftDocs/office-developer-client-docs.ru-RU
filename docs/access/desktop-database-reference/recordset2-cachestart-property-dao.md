---
title: Свойство Recordset2. CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307422"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="a5e47-102">Свойство Recordset2. CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5e47-102">Recordset2.CacheStart property (DAO)</span></span>


<span data-ttu-id="a5e47-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5e47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5e47-104">Задает или возвращает значение, которое определяет закладку первой записи в объекте Recordset типа dynaset, содержащих данные, локально кэшируемые из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a5e47-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e47-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5e47-105">Syntax</span></span>

<span data-ttu-id="a5e47-106">*Expression* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="a5e47-106">*expression* .CacheStart</span></span>

<span data-ttu-id="a5e47-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a5e47-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e47-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5e47-108">Remarks</span></span>

<span data-ttu-id="a5e47-109">Кэширование данных повышает производительность, если вы используете объекты **Recordset** для получения данных с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="a5e47-109">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="a5e47-110">Кэш — это пространство в локальной памяти, в котором хранятся данные, которые были получены последними с сервера. Это полезно, если пользователи запрашивают данные еще раз во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="a5e47-110">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="a5e47-111">Когда пользователи запрашивают данные, ядро СУБД Microsoft Access сначала проверяет кэш для запрошенных данных, а не извлекает его с сервера, что занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="a5e47-111">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="a5e47-112">Кэш сохраняет данные, поступающие из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a5e47-112">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="a5e47-113">Любой источник данных ODBC, подключенный к ядру СУБД Microsoft Access (например, связанная таблица), может иметь локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="a5e47-113">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="a5e47-114">Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, задайте свойства **CacheSize** и **[CacheStart](recordset2-cachestart-property-dao.md)** , а затем используйте метод **[FillCache](recordset2-fillcache-method-dao.md)** или Пошаговое перемещение записей с помощью методов **Move** .</span><span class="sxs-lookup"><span data-stu-id="a5e47-114">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="a5e47-115">Значение свойства **CacheStart** — это закладка первой записи в объекте **Recordset** для кэширования.</span><span class="sxs-lookup"><span data-stu-id="a5e47-115">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached.</span></span> <span data-ttu-id="a5e47-116">Можно использовать закладку любой записи, чтобы задать свойство **CacheStart** .</span><span class="sxs-lookup"><span data-stu-id="a5e47-116">You can use the bookmark of any record to set the **CacheStart** property.</span></span> <span data-ttu-id="a5e47-117">Сделайте запись, которую необходимо запустить, кэшировать текущую запись, и присвойте свойству **CacheStart** значение, равное свойству **[Bookmark](recordset2-bookmark-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a5e47-117">Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="a5e47-118">Ядро СУБД Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="a5e47-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="a5e47-119">Записи, извлеченные из кэша, не отражают изменений, внесенных в исходные данные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="a5e47-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="a5e47-120">Чтобы принудительно обновить все кэшированные данные, задайте для свойства **CacheSize** объекта **Recordset** значение 0, повторно задайте для него размер кэша, который вы изначально запросили, а затем используйте метод **FillCache** .</span><span class="sxs-lookup"><span data-stu-id="a5e47-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

