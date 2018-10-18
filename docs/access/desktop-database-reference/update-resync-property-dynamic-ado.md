---
title: Update Resync Property--Dynamic (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4eea391e99202eeb075d73daa1034dff2042e49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604423"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="457df-102">Update Resync Property--Dynamic (ADO)</span><span class="sxs-lookup"><span data-stu-id="457df-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="457df-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="457df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="457df-104">Указывает, будет ли метод [UpdateBatch](updatebatch-method-ado.md) следуют неявных [выполнить повторную синхронизацию](resync-method-ado.md) метод операцию и если да, области действия этой операции.</span><span class="sxs-lookup"><span data-stu-id="457df-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

<span data-ttu-id="457df-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="457df-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="457df-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="457df-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="457df-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="457df-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="457df-108">master</span><span class="sxs-lookup"><span data-stu-id="457df-108">master</span></span>

<span data-ttu-id="457df-109">Задает или возвращает один или несколько [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) значения.</span><span class="sxs-lookup"><span data-stu-id="457df-109">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="457df-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="457df-110">Remarks</span></span>

<span data-ttu-id="457df-111">Значения ADCPROP\_UPDATERESYNC\_ENUM может быть объединен, за исключением adResyncAll, который уже представляет сочетание остальные значения.</span><span class="sxs-lookup"><span data-stu-id="457df-111">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="457df-112">Константы **adResyncConflicts** хранятся значения повторной синхронизации как базового значения, но не переопределяет ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="457df-112">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="457df-113">**Обновление выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [набора записей](recordset-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="457df-113">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

