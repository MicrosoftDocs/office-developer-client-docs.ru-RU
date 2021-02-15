---
title: Свойство EditMode (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293611"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="4fa56-102">Свойство EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="4fa56-102">EditMode property (ADO)</span></span>


<span data-ttu-id="4fa56-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fa56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fa56-104">Указывает состояние редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4fa56-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="4fa56-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fa56-105">Return value</span></span>

<span data-ttu-id="4fa56-106">Возвращает значение [EditModeEnum.](editmodeenum.md)</span><span class="sxs-lookup"><span data-stu-id="4fa56-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fa56-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="4fa56-107">Remarks</span></span>

<span data-ttu-id="4fa56-108">ADO поддерживает буфер редактирования, связанный с текущей записью.</span><span class="sxs-lookup"><span data-stu-id="4fa56-108">ADO maintains an editing buffer associated with the current record.</span></span> <span data-ttu-id="4fa56-109">Это свойство указывает, были ли внесены изменения в этот буфер или создана ли новая запись.</span><span class="sxs-lookup"><span data-stu-id="4fa56-109">This property indicates whether changes have been made to this buffer, or whether a new record has been created.</span></span> <span data-ttu-id="4fa56-110">Используйте свойство **EditMode,** чтобы определить состояние редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4fa56-110">Use the **EditMode** property to determine the editing status of the current record.</span></span> <span data-ttu-id="4fa56-111">Вы можете проверить ожидающие изменения, если процесс редактирования был прерван, и определить, нужно ли использовать метод [Update](update-method-ado.md) или [CancelUpdate.](cancelupdate-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4fa56-111">You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="4fa56-112">Более подробное описание свойства **EditMode** при различных условиях редактирования см. в методе [AddNew.](addnew-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4fa56-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="4fa56-113">Если вызов [](delete-method-ado-recordset.md) delete не удалит запись или записи в источнике данных (например, из-за нарушения целостности ссылок), набор [recordset](recordset-object-ado.md) останется в режиме редактирования **(EditMode**  =  **adEditInProgress).**</span><span class="sxs-lookup"><span data-stu-id="4fa56-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="4fa56-114">Это означает, что **cancelUpdate** должен быть вызван перед перемещением текущей записи (например, [с Move,](move-method-ado.md) [NextRecordset](nextrecordset-method-ado.md)или [Close).](close-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4fa56-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="4fa56-115">**EditMode** может возвращать допустимые значения, только если существует текущая запись.</span><span class="sxs-lookup"><span data-stu-id="4fa56-115">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="4fa56-116">**EditMode** возвращает ошибку, если [boF или EOF](bof-eof-properties-ado.md) имеет true или если текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="4fa56-116">**EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


