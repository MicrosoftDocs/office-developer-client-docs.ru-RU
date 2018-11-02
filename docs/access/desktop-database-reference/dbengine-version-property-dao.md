---
title: Свойство DBEngine.Version (DAO)
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
ms.openlocfilehash: 1723deea7f29c59fb388a11acc5e5ffcced4abe1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924598"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="e7379-102">Свойство DBEngine.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="e7379-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="e7379-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7379-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7379-104">Возвращает версию DAO в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="e7379-104">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="e7379-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="e7379-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7379-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7379-106">Syntax</span></span>

<span data-ttu-id="e7379-107">*выражение* . Версия</span><span class="sxs-lookup"><span data-stu-id="e7379-107">*expression* .Version</span></span>

<span data-ttu-id="e7379-108">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="e7379-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7379-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7379-109">Remarks</span></span>

<span data-ttu-id="e7379-110">Возвращаемое значение — это строка, которое оценивается как номер версии в форме «major.minor».</span><span class="sxs-lookup"><span data-stu-id="e7379-110">The return value is a String that evaluates to a version number in the form "major.minor".</span></span> <span data-ttu-id="e7379-111">Например «3.0».</span><span class="sxs-lookup"><span data-stu-id="e7379-111">For example, "3.0".</span></span> <span data-ttu-id="e7379-112">Номер версии продукта состоит из номера версии (3), за период и номер версии (0).</span><span class="sxs-lookup"><span data-stu-id="e7379-112">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

