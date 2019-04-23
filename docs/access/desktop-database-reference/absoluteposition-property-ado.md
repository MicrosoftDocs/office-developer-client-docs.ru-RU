---
title: Свойство AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281979"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="1142c-102">Свойство AbsolutePosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="1142c-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="1142c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1142c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1142c-104">Указывает порядковое положение текущей записи объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1142c-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1142c-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1142c-105">Settings and return values</span></span>

<span data-ttu-id="1142c-106">Задает или возвращает значение **типа Long** от 1 до количества записей в объекте **Recordset** ([RecordCount](recordcount-property-ado.md)) или возвращает одно из значений [поситионенум](positionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="1142c-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1142c-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="1142c-107">Remarks</span></span>

<span data-ttu-id="1142c-108">Чтобы задать свойство **AbsolutePosition** , для ADO необходимо, чтобы поставщик OLE DB, который вы используете, реализовал интерфейс ировсетлокате.</span><span class="sxs-lookup"><span data-stu-id="1142c-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="1142c-109">При доступе к свойству **AbsolutePosition** объекта **Recordset** , открытого с помощью однонаправленного или динамического курсора, возникает ошибка **адеррфеатуренотаваилабле**.</span><span class="sxs-lookup"><span data-stu-id="1142c-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span></span> <span data-ttu-id="1142c-110">В случае с другими типами курсора правильное положение будет возвращено, если поставщик поддерживает интерфейс Ировсетскролл.</span><span class="sxs-lookup"><span data-stu-id="1142c-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span></span> <span data-ttu-id="1142c-111">Если поставщик не поддерживает интерфейс *ировсетскролл* , свойству присваивается значение **адпосункновн**.</span><span class="sxs-lookup"><span data-stu-id="1142c-111">If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**.</span></span> <span data-ttu-id="1142c-112">Обратитесь к документации поставщика, чтобы определить, поддерживает ли он *ировсетскролл*.</span><span class="sxs-lookup"><span data-stu-id="1142c-112">See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="1142c-113">Используйте свойство **AbsolutePosition** для перехода к записи на основе ее порядкового номера в объекте **Recordset** или для определения порядкового номера текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1142c-113">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record.</span></span> <span data-ttu-id="1142c-114">Чтобы это свойство было доступно, поставщик должен поддерживать соответствующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="1142c-114">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="1142c-115">Как и свойство [AbsolutePage](absolutepage-property-ado.md) , **AbsolutePosition** имеет значение 1 и равняется 1, если текущая запись является первой записью в наборе **записей**.</span><span class="sxs-lookup"><span data-stu-id="1142c-115">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="1142c-116">Можно получить общее количество записей в объекте **Recordset** из свойства [RecordCount](recordcount-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1142c-116">You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="1142c-117">Когда вы задаете свойство **AbsolutePosition** , даже если оно относится к записи в текущем КЭШЕ, ADO перезагружает кэш с новой группой записей, начиная с указанной записи.</span><span class="sxs-lookup"><span data-stu-id="1142c-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="1142c-118">Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.</span><span class="sxs-lookup"><span data-stu-id="1142c-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="1142c-119">Не следует использовать свойство **AbsolutePosition** в качестве номера записи заместителя.</span><span class="sxs-lookup"><span data-stu-id="1142c-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="1142c-120">Положение заданной записи изменяется при удалении предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="1142c-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="1142c-121">Кроме того, не существует гарантии того, что данная запись будет иметь такой же **AbsolutePosition** при повторном запросе или повторном открытии объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1142c-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="1142c-122">Закладки по-прежнему являются рекомендуемым способом сохранения и возврата к заданному положению и являются единственным способом позиционирования всех типов объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1142c-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


