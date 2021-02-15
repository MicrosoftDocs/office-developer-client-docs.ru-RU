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
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="df572-102">Свойство QueryDef.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="df572-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="df572-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df572-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df572-104">Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально.</span><span class="sxs-lookup"><span data-stu-id="df572-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="df572-105">Для чтения и записи, **Long**.</span><span class="sxs-lookup"><span data-stu-id="df572-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="df572-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df572-106">Syntax</span></span>

<span data-ttu-id="df572-107">*выражение .* CacheSize</span><span class="sxs-lookup"><span data-stu-id="df572-107">*expression* .CacheSize</span></span>

<span data-ttu-id="df572-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="df572-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df572-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="df572-109">Remarks</span></span>

<span data-ttu-id="df572-110">Значение свойства **CacheSize** должно быть от 5 до 1200, но не больше, чем позволяет доступная память.</span><span class="sxs-lookup"><span data-stu-id="df572-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="df572-111">Обычно используется значение 100.</span><span class="sxs-lookup"><span data-stu-id="df572-111">A typical value is 100.</span></span> <span data-ttu-id="df572-112">Если параметр имеет 0, кэшинг отключается.</span><span class="sxs-lookup"><span data-stu-id="df572-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="df572-113">Механизм баз данных Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="df572-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="df572-114">Записи, полученные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="df572-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

