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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708671"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="87f96-102">Метод Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="87f96-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="87f96-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87f96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87f96-104">Изменение пароля существующей базы данных ядра базы данных Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="87f96-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="87f96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87f96-105">Syntax</span></span>

<span data-ttu-id="87f96-106">*выражение* . Новый_пароль (***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="87f96-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="87f96-107">*выражение* Выражение, возвращающее объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="87f96-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="87f96-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="87f96-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87f96-109">Имя</span><span class="sxs-lookup"><span data-stu-id="87f96-109">Name</span></span></p></th>
<th><p><span data-ttu-id="87f96-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="87f96-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="87f96-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="87f96-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="87f96-112">Описание</span><span class="sxs-lookup"><span data-stu-id="87f96-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87f96-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="87f96-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="87f96-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="87f96-114">Required</span></span></p></td>
<td><p><span data-ttu-id="87f96-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="87f96-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="87f96-116">Текущего значения свойства <strong>Password</strong> объекта <strong>базы данных</strong> .</span><span class="sxs-lookup"><span data-stu-id="87f96-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87f96-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="87f96-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="87f96-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="87f96-118">Required</span></span></p></td>
<td><p><span data-ttu-id="87f96-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="87f96-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="87f96-120">Новый параметр <strong>Password</strong> свойство объекта <strong>базы данных</strong> .</span><span class="sxs-lookup"><span data-stu-id="87f96-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="87f96-121"><strong>Примечание</strong>: используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="87f96-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="87f96-122">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="87f96-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="87f96-123">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="87f96-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="87f96-124">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="87f96-124">Weak password: House27.</span></span> <span data-ttu-id="87f96-125">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="87f96-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="87f96-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="87f96-126">Remarks</span></span>

<span data-ttu-id="87f96-127">Строки bstrOld и bstrNew может иметь длину до 20 символов и может содержать все символы, за исключением символа ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="87f96-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="87f96-128">Чтобы удалить пароль, используйте строку нулевой длины ("») для bstrNew.</span><span class="sxs-lookup"><span data-stu-id="87f96-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="87f96-129">Пароли зависят от регистра символов.</span><span class="sxs-lookup"><span data-stu-id="87f96-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="87f96-130">Если базы данных не имеет пароля, ядро базы данных Microsoft Access автоматически создаст, передав строку нулевой длины ("») для старого пароля.</span><span class="sxs-lookup"><span data-stu-id="87f96-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="87f96-131">Если пароль утерян, могут никогда не откройте базу данных еще раз.</span><span class="sxs-lookup"><span data-stu-id="87f96-131">If you lose your password, you can never open the database again.</span></span>


