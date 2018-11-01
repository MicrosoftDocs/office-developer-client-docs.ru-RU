---
title: QueryDef.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 827e0c751101ca68246278c04a408731b77c36a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885124"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="6dfd1-102">QueryDef.CacheSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6dfd1-102">QueryDef.CacheSize Property (DAO)</span></span>


<span data-ttu-id="6dfd1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dfd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6dfd1-104">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="6dfd1-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfd1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6dfd1-106">Syntax</span></span>

<span data-ttu-id="6dfd1-107">*выражение* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="6dfd1-107">*expression* .CacheSize</span></span>

<span data-ttu-id="6dfd1-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="6dfd1-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dfd1-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6dfd1-109">Remarks</span></span>

<span data-ttu-id="6dfd1-110">Значение свойства **CacheSize** должен быть между 5 и 1200, но не больше, чем объем доступной памяти будет разрешено.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="6dfd1-111">Стандартное значение равно 100.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-111">A typical value is 100.</span></span> <span data-ttu-id="6dfd1-112">Значение 0 отключает кэширование.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="6dfd1-113">Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="6dfd1-114">Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

