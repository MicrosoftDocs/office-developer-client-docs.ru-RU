---
title: Свойство Prepared (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718072"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="ca9ab-102">Свойство Prepared (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca9ab-102">Prepared property (ADO)</span></span>


<span data-ttu-id="ca9ab-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca9ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca9ab-104">Указывает, следует ли сохранять версии скомпилированной перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ca9ab-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ca9ab-105">Settings and return values</span></span>

<span data-ttu-id="ca9ab-106">Задает или возвращает **логическое** значение, которые, если задано значение **True**, указывает, что команда должна подготовлен.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca9ab-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca9ab-107">Remarks</span></span>

<span data-ttu-id="ca9ab-108">Используйте свойство **подготовленных** для поставщика данных сохранить готовую (или скомпилированную) версию запроса, указанных в свойстве [CommandText](commandtext-property-ado.md) до выполнения первого объекта [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ca9ab-108">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution.</span></span> <span data-ttu-id="ca9ab-109">Это может снизить первого выполнения команды, но после поставщик компилирует команды, поставщик будет использовать версии скомпилированной команды для любого при последующих вызовах, которые приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-109">This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="ca9ab-110">Если свойство имеет **значение False**, поставщик будет выполняться **команда** объект напрямую без создания версии скомпилированной.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="ca9ab-111">Если поставщик поддерживает команды подготовки, может возвращает ошибку, как только это свойство имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-111">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**.</span></span> <span data-ttu-id="ca9ab-112">Если он не возвращает ошибку, он просто игнорирует запрос на подготовку команды и устанавливает для свойства **подготовленных** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-112">If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

