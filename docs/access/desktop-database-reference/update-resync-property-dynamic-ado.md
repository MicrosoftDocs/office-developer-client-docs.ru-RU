---
title: Обновление свойства динамического повторной синхронизации (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702028"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="ad8d0-102">Обновление свойства динамического повторной синхронизации (ADO)</span><span class="sxs-lookup"><span data-stu-id="ad8d0-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="ad8d0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad8d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad8d0-104">Указывает, будет ли метод [UpdateBatch](updatebatch-method-ado.md) следуют неявных [выполнить повторную синхронизацию](resync-method-ado.md) метод операцию и если да, области действия этой операции.</span><span class="sxs-lookup"><span data-stu-id="ad8d0-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ad8d0-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ad8d0-105">Settings and return values</span></span>

<span data-ttu-id="ad8d0-106">Задает или возвращает один или несколько [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) значения.</span><span class="sxs-lookup"><span data-stu-id="ad8d0-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad8d0-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="ad8d0-107">Remarks</span></span>

<span data-ttu-id="ad8d0-108">Значения ADCPROP\_UPDATERESYNC\_ENUM может быть объединен, за исключением adResyncAll, который уже представляет сочетание остальные значения.</span><span class="sxs-lookup"><span data-stu-id="ad8d0-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="ad8d0-109">Константы **adResyncConflicts** хранятся значения повторной синхронизации как базового значения, но не переопределяет ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="ad8d0-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="ad8d0-110">**Обновление выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [набора записей](recordset-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="ad8d0-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

