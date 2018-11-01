---
title: Свойство EditMode (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c859d85dc62e09a1fd21af11deaca5d0f2e8b85
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867351"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="e7a66-102">Свойство EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7a66-102">EditMode property (ADO)</span></span>


<span data-ttu-id="e7a66-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7a66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7a66-104">Указывает состояние редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e7a66-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7a66-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7a66-105">Return value</span></span>

<span data-ttu-id="e7a66-106">Возвращает значение [EditModeEnum](editmodeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e7a66-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7a66-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7a66-107">Remarks</span></span>

<span data-ttu-id="e7a66-108">ADO поддерживает редактирования буфера, связанного с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e7a66-108">ADO maintains an editing buffer associated with the current record.</span></span> <span data-ttu-id="e7a66-109">Это свойство показывает ли изменения были внесены в этот буфер или создан ли новую запись.</span><span class="sxs-lookup"><span data-stu-id="e7a66-109">This property indicates whether changes have been made to this buffer, or whether a new record has been created.</span></span> <span data-ttu-id="e7a66-110">Свойство **EditMode** используется для определения статуса редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e7a66-110">Use the **EditMode** property to determine the editing status of the current record.</span></span> <span data-ttu-id="e7a66-111">Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать [обновления](update-method-ado.md) или метод [CancelUpdate](cancelupdate-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e7a66-111">You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="e7a66-112">В разделе метод [AddNew](addnew-method-ado.md) более подробное описание свойства **EditMode** в различных условиях редактирования.</span><span class="sxs-lookup"><span data-stu-id="e7a66-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="e7a66-113">Когда звонка для [удаления](delete-method-ado-recordset.md) успешно не удалять записи или записей в данных источника (из-за нарушения ссылочной целостности, например), [записей](recordset-object-ado.md) останется в режиме редактирования (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="e7a66-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="e7a66-114">Это означает, что **CancelUpdate** необходимо вызывать перед перемещением off текущей записи (с [перемещением](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)и [Закрыть](close-method-ado.md), например).</span><span class="sxs-lookup"><span data-stu-id="e7a66-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="e7a66-115">**EditMode** можно вернуть допустимое значение только в том случае, если текущая запись.</span><span class="sxs-lookup"><span data-stu-id="e7a66-115">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="e7a66-116">**EditMode** возвращает ошибку, если [BOF или EOF](bof-eof-properties-ado.md) имеет значение true, или если текущий запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="e7a66-116">**EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


