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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722685"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="f6352-102">Свойство Workspace.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="f6352-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="f6352-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6352-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6352-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="f6352-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="f6352-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="f6352-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6352-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6352-106">Syntax</span></span>

<span data-ttu-id="f6352-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="f6352-107">*expression* .Type</span></span>

<span data-ttu-id="f6352-108">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="f6352-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6352-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6352-109">Remarks</span></span>

<span data-ttu-id="f6352-110">Для объекта **рабочей области** возможные параметры и возвращаемые значения, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f6352-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6352-111">Константа</span><span class="sxs-lookup"><span data-stu-id="f6352-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="f6352-112">Тип рабочей области</span><span class="sxs-lookup"><span data-stu-id="f6352-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6352-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="f6352-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="f6352-114"><strong>Рабочая область для</strong> подключенных к ядру базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f6352-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6352-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="f6352-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="f6352-116"><strong>Рабочая область для</strong> подключенных к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="f6352-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

