---
title: Свойство DBEngine.DefaultType (DAO)
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
ms.openlocfilehash: ec8dbc1e758b19c15c1a08b9936fa3c00acabde6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925662"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="f2921-102">Свойство DBEngine.DefaultType (DAO)</span><span class="sxs-lookup"><span data-stu-id="f2921-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="f2921-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2921-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2921-104">Задает или возвращает значение, указывающее, какой тип рабочей области будет использоваться далее созданный объект **[рабочей области](workspace-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f2921-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2921-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2921-105">Syntax</span></span>

<span data-ttu-id="f2921-106">*выражение* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="f2921-106">*expression* .DefaultType</span></span>

<span data-ttu-id="f2921-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="f2921-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2921-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2921-108">Remarks</span></span>

<span data-ttu-id="f2921-109">Параметр или возвращаемое значение может быть одним из **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** констант.</span><span class="sxs-lookup"><span data-stu-id="f2921-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="f2921-110">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="f2921-110">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="f2921-111">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f2921-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="f2921-112">Параметр может быть переопределен для одной **рабочей области** путем установки для параметра метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** аргумент типа.</span><span class="sxs-lookup"><span data-stu-id="f2921-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

