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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301094"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="11984-102">Свойство QueryDef.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="11984-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="11984-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11984-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11984-104">Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально.</span><span class="sxs-lookup"><span data-stu-id="11984-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="11984-105">Для чтения и записи, **Long**.</span><span class="sxs-lookup"><span data-stu-id="11984-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11984-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11984-106">Syntax</span></span>

<span data-ttu-id="11984-107">*выражения* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="11984-107">*expression* .CacheSize</span></span>

<span data-ttu-id="11984-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="11984-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="11984-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="11984-109">Remarks</span></span>

<span data-ttu-id="11984-110">Значение свойства **CacheSize** должно быть от 5 до 1200, но не больше, чем позволяет доступная память.</span><span class="sxs-lookup"><span data-stu-id="11984-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="11984-111">Обычное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="11984-111">A typical value is 100.</span></span> <span data-ttu-id="11984-112">Параметр 0 отключит кэшинг.</span><span class="sxs-lookup"><span data-stu-id="11984-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="11984-113">Двигатель базы данных Microsoft Access запрашивает записи в кэше в диапазоне от кэша, а записи за пределами кэша запрашивает сервер.</span><span class="sxs-lookup"><span data-stu-id="11984-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="11984-114">Записи, извлеченные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="11984-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

