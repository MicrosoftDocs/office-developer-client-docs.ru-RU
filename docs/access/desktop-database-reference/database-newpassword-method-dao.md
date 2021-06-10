---
title: Метод Database.NewPassword (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294857"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="5c259-102">Метод Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c259-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="5c259-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c259-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c259-104">Изменяет пароль существующей базы данных базы данных Microsoft Access (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5c259-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c259-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c259-105">Syntax</span></span>

<span data-ttu-id="5c259-106">*выражения* . NewPassword ***(bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="5c259-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="5c259-107">*выражение* Выражение, возвращаемая **объекту Database.**</span><span class="sxs-lookup"><span data-stu-id="5c259-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c259-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c259-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c259-109">Имя</span><span class="sxs-lookup"><span data-stu-id="5c259-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5c259-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="5c259-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5c259-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5c259-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5c259-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5c259-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c259-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="5c259-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="5c259-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5c259-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5c259-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="5c259-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5c259-116">Текущий параметр свойства <strong>Password</strong> объекта <strong>Database.</strong></span><span class="sxs-lookup"><span data-stu-id="5c259-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c259-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="5c259-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="5c259-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5c259-118">Required</span></span></p></td>
<td><p><span data-ttu-id="5c259-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="5c259-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5c259-120">Новый параметр свойства <strong>Password</strong> объекта <strong>Database.</strong></span><span class="sxs-lookup"><span data-stu-id="5c259-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="5c259-121"><strong>ПРИМЕЧАНИЕ.</strong>Используйте надежные пароли, сочетая в себе буквы, цифры и символы верхнего и нижнего регистров.</span><span class="sxs-lookup"><span data-stu-id="5c259-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="5c259-122">В ненадежных паролях не используются сочетания таких элементов.</span><span class="sxs-lookup"><span data-stu-id="5c259-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="5c259-123">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="5c259-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="5c259-124">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="5c259-124">Weak password: House27.</span></span> <span data-ttu-id="5c259-125">Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</span><span class="sxs-lookup"><span data-stu-id="5c259-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5c259-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c259-126">Remarks</span></span>

<span data-ttu-id="5c259-127">Строки bstrOld и bstrNew могут быть длиной до 20 символов и могут включать любые символы, кроме символа ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5c259-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="5c259-128">Чтобы очистить пароль, используйте строку нулевой длины ("") для bstrNew.</span><span class="sxs-lookup"><span data-stu-id="5c259-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="5c259-129">В паролях учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="5c259-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="5c259-130">Если в базе данных нет пароля, то двигатель базы данных Microsoft Access автоматически создает его, передав строку нулевой длины ("") для старого пароля.</span><span class="sxs-lookup"><span data-stu-id="5c259-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="5c259-131">Если вы потеряете пароль, вы никогда не сможете открыть базу данных снова.</span><span class="sxs-lookup"><span data-stu-id="5c259-131">If you lose your password, you can never open the database again.</span></span>


