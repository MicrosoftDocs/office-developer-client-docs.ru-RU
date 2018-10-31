---
title: Добавление пользователя оператора (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 80e3a8fe62cf077accfc18a30e188898fb279d1d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862291"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="6a600-102">Добавление пользователя оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6a600-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="6a600-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a600-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a600-104">Добавление одного или нескольких существующих *пользователей*s существующей *группы*.</span><span class="sxs-lookup"><span data-stu-id="6a600-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a600-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a600-105">Syntax</span></span>

<span data-ttu-id="6a600-106">Добавление пользователя *пользователя*\[, *пользователь*... \] В *группу*</span><span class="sxs-lookup"><span data-stu-id="6a600-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="6a600-107">Оператор добавить пользователя состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="6a600-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a600-108">Часть</span><span class="sxs-lookup"><span data-stu-id="6a600-108">Part</span></span></p></th>
<th><p><span data-ttu-id="6a600-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6a600-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a600-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="6a600-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="6a600-111">Имя пользователя для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="6a600-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a600-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="6a600-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="6a600-113">Имя группы для добавления файла рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="6a600-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6a600-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a600-114">Remarks</span></span>

<span data-ttu-id="6a600-115">После *пользователь* добавлен в *группу*, *пользователь* имеет все разрешения, предоставленные в *группу*.</span><span class="sxs-lookup"><span data-stu-id="6a600-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

