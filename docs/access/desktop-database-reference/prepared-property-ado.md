---
title: Prepared Property (ADO)
TOCTitle: Prepared Property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865453f89cd5942ec7f9f8d036beb72dc519397e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480053"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="c583b-102">Prepared Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="c583b-102">Prepared Property (ADO)</span></span>


<span data-ttu-id="c583b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c583b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c583b-104">Указывает, следует ли сохранять версии скомпилированной перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="c583b-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c583b-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c583b-105">Settings and Return Values</span></span>

<span data-ttu-id="c583b-106">Задает или возвращает **логическое** значение, которые, если задано значение **True**, указывает, что команда должна подготовлен.</span><span class="sxs-lookup"><span data-stu-id="c583b-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="c583b-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="c583b-107">Remarks</span></span>

<span data-ttu-id="c583b-108">Используйте свойство **подготовленных** для поставщика данных сохранить готовую (или скомпилированную) версию запроса, указанных в свойстве [CommandText](commandtext-property-ado.md) до выполнения первого объекта [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c583b-108">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution.</span></span> <span data-ttu-id="c583b-109">Это может снизить первого выполнения команды, но после поставщик компилирует команды, поставщик будет использовать версии скомпилированной команды для любого при последующих вызовах, которые приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="c583b-109">This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="c583b-110">Если свойство имеет **значение False**, поставщик будет выполняться **команда** объект напрямую без создания версии скомпилированной.</span><span class="sxs-lookup"><span data-stu-id="c583b-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="c583b-111">Если поставщик поддерживает команды подготовки, может возвращает ошибку, как только это свойство имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="c583b-111">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**.</span></span> <span data-ttu-id="c583b-112">Если он не возвращает ошибку, он просто игнорирует запрос на подготовку команды и устанавливает для свойства **подготовленных** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="c583b-112">If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

