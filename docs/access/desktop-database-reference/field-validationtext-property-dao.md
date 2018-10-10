---
title: Field.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fcdcd3d7e052dc2d04b34089b7b4f02896fb339a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480879"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="506f3-102">Field.ValidationText Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="506f3-102">Field.ValidationText Property (DAO)</span></span>


<span data-ttu-id="506f3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="506f3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="506f3-104">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение **поля** объекта не удовлетворяют правило проверки, указанного идентификатором **условие на значение** свойства поля (только для рабочих областей Microsoft Access) .</span><span class="sxs-lookup"><span data-stu-id="506f3-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="506f3-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="506f3-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="506f3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="506f3-106">Syntax</span></span>

<span data-ttu-id="506f3-107">*выражение* . Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="506f3-107">*expression* .ValidationText</span></span>

<span data-ttu-id="506f3-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="506f3-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="506f3-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="506f3-109">Remarks</span></span>

<span data-ttu-id="506f3-110">Параметр или возвращаемое значение — это **строка** , которая определяет текст, который отображается, если пользователь пытается ввести недопустимое значение для поля.</span><span class="sxs-lookup"><span data-stu-id="506f3-110">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field.</span></span> <span data-ttu-id="506f3-111">Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="506f3-111">For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="506f3-112">Использование свойства **сообщение об ошибке** для объекта **поля** зависит от объекта, который содержит коллекцию **[полей](fields-collection-dao.md)** , к которому добавляется объект **поля** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="506f3-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="506f3-113">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="506f3-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="506f3-114">Применение</span><span class="sxs-lookup"><span data-stu-id="506f3-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="506f3-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="506f3-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="506f3-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="506f3-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="506f3-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="506f3-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="506f3-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="506f3-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="506f3-119"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="506f3-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="506f3-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="506f3-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="506f3-121"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="506f3-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="506f3-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="506f3-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="506f3-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="506f3-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="506f3-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="506f3-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

