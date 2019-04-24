---
title: Метод Database. NewPassword (DAO)
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
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="53171-102">Метод Database. NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="53171-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="53171-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53171-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53171-104">Изменяет пароль существующей базы данных ядра СУБД Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="53171-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="53171-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53171-105">Syntax</span></span>

<span data-ttu-id="53171-106">*Expression* . NewPassword (***бстролд***, ***бстрнев***)</span><span class="sxs-lookup"><span data-stu-id="53171-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="53171-107">*Expression (выражение* ) Выражение, возвращающее объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="53171-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="53171-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53171-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53171-109">Имя</span><span class="sxs-lookup"><span data-stu-id="53171-109">Name</span></span></p></th>
<th><p><span data-ttu-id="53171-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="53171-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="53171-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="53171-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="53171-112">Описание</span><span class="sxs-lookup"><span data-stu-id="53171-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53171-113"><em>Бстролд</em></span><span class="sxs-lookup"><span data-stu-id="53171-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="53171-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="53171-114">Required</span></span></p></td>
<td><p><span data-ttu-id="53171-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="53171-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="53171-116">Текущее значение свойства <strong>Password</strong> объекта <strong>Database</strong> .</span><span class="sxs-lookup"><span data-stu-id="53171-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53171-117"><em>Бстрнев</em></span><span class="sxs-lookup"><span data-stu-id="53171-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="53171-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="53171-118">Required</span></span></p></td>
<td><p><span data-ttu-id="53171-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="53171-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="53171-120">Новый параметр свойства <strong>Password</strong> объекта <strong>Database</strong> .</span><span class="sxs-lookup"><span data-stu-id="53171-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="53171-121"><strong>Note</strong>: Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы.</span><span class="sxs-lookup"><span data-stu-id="53171-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="53171-122">В слабых паролях эти элементы не комбинируются.</span><span class="sxs-lookup"><span data-stu-id="53171-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="53171-123">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="53171-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="53171-124">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="53171-124">Weak password: House27.</span></span> <span data-ttu-id="53171-125">Используйте надежный пароль, который можно запомнить, чтобы не записывать его.</span><span class="sxs-lookup"><span data-stu-id="53171-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="53171-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="53171-126">Remarks</span></span>

<span data-ttu-id="53171-127">Строки Бстролд и Бстрнев могут иметь длину до 20 символов и могут содержать любые символы, кроме символов ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="53171-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="53171-128">Чтобы очистить пароль, используйте строку нулевой длины ("") для Бстрнев.</span><span class="sxs-lookup"><span data-stu-id="53171-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="53171-129">В паролях учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="53171-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="53171-130">Если база данных не имеет пароля, ядро СУБД Microsoft Access автоматически создаст ее, передав для старого пароля строку нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="53171-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="53171-131">Если вы потеряли пароль, вы не сможете повторно открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="53171-131">If you lose your password, you can never open the database again.</span></span>


