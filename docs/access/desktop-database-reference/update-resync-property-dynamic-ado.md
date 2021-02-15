---
title: Обновление динамического свойства Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308346"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="a2549-102">Обновление динамического свойства Resync (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2549-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="a2549-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2549-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2549-104">Указывает, следует ли за [методом UpdateBatch](updatebatch-method-ado.md) неявную операцию метода [Resync](resync-method-ado.md) и, если да, область этой операции.</span><span class="sxs-lookup"><span data-stu-id="a2549-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a2549-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a2549-105">Settings and return values</span></span>

<span data-ttu-id="a2549-106">Задает или возвращает одно или несколько значений [ENUM ADCPROP \_ UPDATERESYNC. \_ ](adcprop-updateresync-enum.md)</span><span class="sxs-lookup"><span data-stu-id="a2549-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2549-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="a2549-107">Remarks</span></span>

<span data-ttu-id="a2549-108">Значения ENUM ADCPROP UPDATERESYNC могут быть объединены, за исключением \_ adResyncAll, который уже представляет комбинацию остальных \_ значений.</span><span class="sxs-lookup"><span data-stu-id="a2549-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="a2549-109">**Константа adResyncConflicts** сохраняет значения повторной проверки в качестве значений, но не переопределяет ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="a2549-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="a2549-110">**Update Resync** — это динамическое свойство, [](properties-collection-ado.md) которое применится к коллекции свойств объекта [Recordset,](recordset-object-ado.md) когда свойству [CursorLocation](cursorlocation-property-ado.md) задано свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="a2549-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

