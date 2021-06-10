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
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294192"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="794ec-102">Свойство DBEngine.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="794ec-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="794ec-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="794ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="794ec-104">Rreturns версия DAO в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="794ec-104">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="794ec-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="794ec-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="794ec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="794ec-106">Syntax</span></span>

<span data-ttu-id="794ec-107">*выражения* . Версия</span><span class="sxs-lookup"><span data-stu-id="794ec-107">*expression* .Version</span></span>

<span data-ttu-id="794ec-108">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="794ec-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="794ec-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="794ec-109">Remarks</span></span>

<span data-ttu-id="794ec-110">Возвращаемая величина — это строка, которая оценивает номер версии в форме "major.minor".</span><span class="sxs-lookup"><span data-stu-id="794ec-110">The return value is a String that evaluates to a version number in the form "major.minor".</span></span> <span data-ttu-id="794ec-111">Например, "3.0".</span><span class="sxs-lookup"><span data-stu-id="794ec-111">For example, "3.0".</span></span> <span data-ttu-id="794ec-112">Номер версии продукта состоит из номера версии (3), периода и номера выпуска (0).</span><span class="sxs-lookup"><span data-stu-id="794ec-112">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

