---
title: Field2.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d971b14093dd02204327e6f0ef30a81c6567c5bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483002"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="de543-102">Field2.ValidationText Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="de543-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="de543-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de543-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de543-104">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение объекта **поле2** не соответствует правило проверки, указанного идентификатором **условие на значение** свойства поля (Microsoft Access рабочие области только ).</span><span class="sxs-lookup"><span data-stu-id="de543-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="de543-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="de543-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="de543-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de543-106">Syntax</span></span>

<span data-ttu-id="de543-107">*выражение* . Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="de543-107">*expression* .ValidationText</span></span>

<span data-ttu-id="de543-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="de543-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de543-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="de543-109">Remarks</span></span>

<span data-ttu-id="de543-110">Параметр или возвращаемое значение — это **строка** , которая определяет текст, который отображается, если пользователь пытается ввести недопустимое значение для поля.</span><span class="sxs-lookup"><span data-stu-id="de543-110">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field.</span></span> <span data-ttu-id="de543-111">Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="de543-111">For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="de543-112">Для объекта **поле2** использование свойства **сообщение об ошибке** зависит от объекта, который содержит коллекцию **[полей](fields-collection-dao.md)** , к которому добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="de543-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de543-113">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="de543-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="de543-114">Применение</span><span class="sxs-lookup"><span data-stu-id="de543-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de543-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="de543-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="de543-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="de543-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de543-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="de543-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="de543-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="de543-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de543-119"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="de543-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="de543-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="de543-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de543-121"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="de543-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="de543-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="de543-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de543-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="de543-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="de543-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="de543-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

