---
title: Свойство QueryDef.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701711"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="3f068-102">Свойство QueryDef.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f068-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="3f068-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f068-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f068-104">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="3f068-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="3f068-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="3f068-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f068-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f068-106">Syntax</span></span>

<span data-ttu-id="3f068-107">*выражение* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="3f068-107">*expression* .CacheSize</span></span>

<span data-ttu-id="3f068-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="3f068-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f068-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f068-109">Remarks</span></span>

<span data-ttu-id="3f068-110">Значение свойства **CacheSize** должен быть между 5 и 1200, но не больше, чем объем доступной памяти будет разрешено.</span><span class="sxs-lookup"><span data-stu-id="3f068-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="3f068-111">Стандартное значение равно 100.</span><span class="sxs-lookup"><span data-stu-id="3f068-111">A typical value is 100.</span></span> <span data-ttu-id="3f068-112">Значение 0 отключает кэширование.</span><span class="sxs-lookup"><span data-stu-id="3f068-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="3f068-113">Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="3f068-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="3f068-114">Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="3f068-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

