---
title: DBEngine.Version Property (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865942cdf4cca81cb0d5348725164a4a75a845fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870914"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="0e544-102">DBEngine.Version Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e544-102">DBEngine.Version Property (DAO)</span></span>


<span data-ttu-id="0e544-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e544-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e544-104">Возвращает версию DAO в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="0e544-104">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="0e544-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="0e544-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e544-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e544-106">Syntax</span></span>

<span data-ttu-id="0e544-107">*выражение* . Версия</span><span class="sxs-lookup"><span data-stu-id="0e544-107">*expression* .Version</span></span>

<span data-ttu-id="0e544-108">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0e544-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e544-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e544-109">Remarks</span></span>

<span data-ttu-id="0e544-110">Возвращаемое значение — это строка, которое оценивается как номер версии в форме «major.minor».</span><span class="sxs-lookup"><span data-stu-id="0e544-110">The return value is a String that evaluates to a version number in the form "major.minor".</span></span> <span data-ttu-id="0e544-111">Например «3.0».</span><span class="sxs-lookup"><span data-stu-id="0e544-111">For example, "3.0".</span></span> <span data-ttu-id="0e544-112">Номер версии продукта состоит из номера версии (3), за период и номер версии (0).</span><span class="sxs-lookup"><span data-stu-id="0e544-112">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

