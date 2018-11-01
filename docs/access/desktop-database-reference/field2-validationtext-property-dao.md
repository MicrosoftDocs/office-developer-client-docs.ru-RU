---
title: Field2.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b8ce99f7fbedc487f5c5bae98745f1d446c2da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867148"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="9272e-102">Field2.ValidationText Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9272e-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="9272e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9272e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9272e-104">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение объекта **поле2** не соответствует правило проверки, указанного идентификатором **условие на значение** свойства поля (Microsoft Access рабочие области только ).</span><span class="sxs-lookup"><span data-stu-id="9272e-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="9272e-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="9272e-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9272e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9272e-106">Syntax</span></span>

<span data-ttu-id="9272e-107">*выражение* . Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="9272e-107">*expression* .ValidationText</span></span>

<span data-ttu-id="9272e-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="9272e-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9272e-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="9272e-109">Remarks</span></span>

<span data-ttu-id="9272e-110">Параметр или возвращаемое значение — это **строка** , которая определяет текст, который отображается, если пользователь пытается ввести недопустимое значение для поля.</span><span class="sxs-lookup"><span data-stu-id="9272e-110">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field.</span></span> <span data-ttu-id="9272e-111">Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9272e-111">For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="9272e-112">Для объекта **поле2** использование свойства **сообщение об ошибке** зависит от объекта, который содержит коллекцию **[полей](fields-collection-dao.md)** , к которому добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9272e-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9272e-113">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="9272e-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="9272e-114">Применение</span><span class="sxs-lookup"><span data-stu-id="9272e-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9272e-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="9272e-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="9272e-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9272e-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9272e-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="9272e-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="9272e-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9272e-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9272e-119"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="9272e-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="9272e-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9272e-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9272e-121"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="9272e-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="9272e-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9272e-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9272e-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="9272e-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="9272e-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9272e-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

