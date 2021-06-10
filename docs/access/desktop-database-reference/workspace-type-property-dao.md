---
title: Свойство Workspace.Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311307"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="0d4b0-102">Свойство Workspace.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d4b0-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="0d4b0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d4b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d4b0-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="0d4b0-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4b0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d4b0-106">Syntax</span></span>

<span data-ttu-id="0d4b0-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="0d4b0-107">*expression* .Type</span></span>

<span data-ttu-id="0d4b0-108">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d4b0-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d4b0-109">Remarks</span></span>

<span data-ttu-id="0d4b0-110">Для объекта **Workspace** возможные параметры и значения возврата следуют следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d4b0-111">Константа</span><span class="sxs-lookup"><span data-stu-id="0d4b0-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0d4b0-112">Тип рабочей области</span><span class="sxs-lookup"><span data-stu-id="0d4b0-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d4b0-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="0d4b0-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="0d4b0-114">Рабочее <strong>пространство подключено</strong> к базе данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d4b0-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="0d4b0-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="0d4b0-116">Рабочее <strong>пространство подключено</strong> к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

