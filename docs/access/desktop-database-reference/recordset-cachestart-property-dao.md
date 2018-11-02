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
ms.openlocfilehash: c73a12803a65f84d11ab62955d80ccda3d0825fb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919180"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="9bc95-102">Свойство Recordset.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="9bc95-102">Recordset.CacheStart property (DAO)</span></span>


<span data-ttu-id="9bc95-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bc95-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bc95-104">Задает или возвращает значение, указывающее закладки для первой записи в объекте типа динамического набора записей, содержащий данные для локально кэшировать из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9bc95-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bc95-105">Syntax</span></span>

<span data-ttu-id="9bc95-106">*выражение* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="9bc95-106">*expression* .CacheStart</span></span>

<span data-ttu-id="9bc95-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9bc95-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bc95-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9bc95-108">Remarks</span></span>

<span data-ttu-id="9bc95-109">Кэширование данных улучшает производительность при использовании **набора записей** объектов для извлечения данных из удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="9bc95-109">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="9bc95-110">Кэш — это должен быть пробел в локальной памяти, в которой содержатся данные, недавно извлеченные с сервера. Это полезно, если пользователи запрашивать данные еще раз во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="9bc95-110">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="9bc95-111">Когда пользователь запрашивает данные, ядро базы данных Microsoft Access кэша для запрошенные данные сначала проверяет вместо извлечение из сервера, который занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="9bc95-111">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="9bc95-112">Кэш сохраняет только данные, поступающие из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9bc95-112">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="9bc95-113">Любой Microsoft Access базы данных подключением модуль ODBC источник данных, например связанной таблицы может иметь локального кэша.</span><span class="sxs-lookup"><span data-stu-id="9bc95-113">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="9bc95-114">Создание кэша, откройте объект **набора записей** из к удаленному источнику данных, задать свойства **CacheSize** и **[CacheStart](recordset-cachestart-property-dao.md)** и затем используйте метод **[FillCache](recordset-fillcache-method-dao.md)** или пошаговое выполнение записи с помощью методов **перемещения** .</span><span class="sxs-lookup"><span data-stu-id="9bc95-114">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="9bc95-115">Значение свойства **CacheStart** — закладки для первой записи в объекте **набора записей** для кэширования.</span><span class="sxs-lookup"><span data-stu-id="9bc95-115">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached.</span></span> <span data-ttu-id="9bc95-116">Закладки для любой записи можно использовать для свойства **CacheStart** .</span><span class="sxs-lookup"><span data-stu-id="9bc95-116">You can use the bookmark of any record to set the **CacheStart** property.</span></span> <span data-ttu-id="9bc95-117">Сделать запись должна быть запущена текущей записи кэша и задайте свойство **CacheStart** свойством **[Закладка](recordset-bookmark-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9bc95-117">Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="9bc95-118">Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="9bc95-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="9bc95-119">Записей, полученных из кэша не отражает изменения, внесенные одновременно исходных данных другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="9bc95-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="9bc95-120">Чтобы принудительно выполнить обновление всех кэшированных данных, значение 0, снова задайте для него значение размера кэша, изначально запрошен, а затем использовать метод **FillCache** свойство **CacheSize** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9bc95-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

