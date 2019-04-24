---
title: Свойство DBEngine. DefaultType (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294381"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="05148-102">Свойство DBEngine. DefaultType (DAO)</span><span class="sxs-lookup"><span data-stu-id="05148-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="05148-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05148-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05148-104">Задает или возвращает значение, указывающее тип рабочей области, который будет использоваться при создании следующего объекта **[Workspace](workspace-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="05148-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="05148-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05148-105">Syntax</span></span>

<span data-ttu-id="05148-106">*Expression* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="05148-106">*expression* .DefaultType</span></span>

<span data-ttu-id="05148-107">*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="05148-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="05148-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="05148-108">Remarks</span></span>

<span data-ttu-id="05148-109">Параметр или возвращаемое значение может быть одной из констант **[воркспацетипинум](workspacetypeenum-enumeration-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="05148-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="05148-110">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="05148-110">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="05148-111">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="05148-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="05148-112">Параметр можно переопределить для отдельной **рабочей области** , задав аргумент Type для метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="05148-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

