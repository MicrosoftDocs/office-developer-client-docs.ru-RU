---
title: QueryDef.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ecddf9a9972c6ded5e28748822169c2c60edc44
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479942"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="2a285-102">QueryDef.CacheSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a285-102">QueryDef.CacheSize Property (DAO)</span></span>


<span data-ttu-id="2a285-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a285-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a285-104">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="2a285-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="2a285-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="2a285-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a285-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a285-106">Syntax</span></span>

<span data-ttu-id="2a285-107">*выражение* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="2a285-107">*expression* .CacheSize</span></span>

<span data-ttu-id="2a285-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2a285-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a285-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a285-109">Remarks</span></span>

<span data-ttu-id="2a285-110">Значение свойства **CacheSize** должен быть между 5 и 1200, но не больше, чем объем доступной памяти будет разрешено.</span><span class="sxs-lookup"><span data-stu-id="2a285-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="2a285-111">Стандартное значение равно 100.</span><span class="sxs-lookup"><span data-stu-id="2a285-111">A typical value is 100.</span></span> <span data-ttu-id="2a285-112">Значение 0 отключает кэширование.</span><span class="sxs-lookup"><span data-stu-id="2a285-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="2a285-113">Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="2a285-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="2a285-114">Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="2a285-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

