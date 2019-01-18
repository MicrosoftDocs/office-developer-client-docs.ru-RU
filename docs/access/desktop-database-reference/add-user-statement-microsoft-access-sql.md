---
title: Добавление пользователя оператора (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705395"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="225e4-102">Добавление пользователя оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="225e4-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="225e4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="225e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="225e4-104">Добавление одного или нескольких существующих *пользователей*s существующей *группы*.</span><span class="sxs-lookup"><span data-stu-id="225e4-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="225e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="225e4-105">Syntax</span></span>

<span data-ttu-id="225e4-106">Добавление пользователя *пользователя*\[, *пользователь*... \] В *группу*</span><span class="sxs-lookup"><span data-stu-id="225e4-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="225e4-107">Оператор добавить пользователя состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="225e4-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="225e4-108">Часть</span><span class="sxs-lookup"><span data-stu-id="225e4-108">Part</span></span></p></th>
<th><p><span data-ttu-id="225e4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="225e4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="225e4-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="225e4-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="225e4-111">Имя пользователя для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="225e4-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225e4-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="225e4-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="225e4-113">Имя группы для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="225e4-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="225e4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="225e4-114">Remarks</span></span>

<span data-ttu-id="225e4-115">После *пользователь* добавлен в *группу*, *пользователь* имеет все разрешения, предоставленные в *группу*.</span><span class="sxs-lookup"><span data-stu-id="225e4-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

