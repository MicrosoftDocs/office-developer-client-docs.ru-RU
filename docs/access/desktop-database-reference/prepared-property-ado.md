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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301458"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="123fa-102">Свойство Prepared (ADO)</span><span class="sxs-lookup"><span data-stu-id="123fa-102">Prepared property (ADO)</span></span>


<span data-ttu-id="123fa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="123fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="123fa-104">Указывает, следует ли сохранять скомпилную версию команды перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="123fa-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="123fa-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="123fa-105">Settings and return values</span></span>

<span data-ttu-id="123fa-106">Задает или возвращает значение **boolean,** которое,если задано значение **True,** указывает на то, что команда должна быть подготовлена.</span><span class="sxs-lookup"><span data-stu-id="123fa-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="123fa-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="123fa-107">Remarks</span></span>

<span data-ttu-id="123fa-108">Используйте свойство **Prepared,** чтобы поставщик мог сохранить подготовленную (или скомпилную) версию [](command-object-ado.md) запроса, указанного в свойстве [CommandText,](commandtext-property-ado.md) перед первым выполнением объекта Command.</span><span class="sxs-lookup"><span data-stu-id="123fa-108">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution.</span></span> <span data-ttu-id="123fa-109">Это может замедлить первое выполнение команды, но после компиляции команды поставщик будет использовать скомпилную версию команды для последующих выполнения, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="123fa-109">This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="123fa-110">Если свойство имеет свойство **False,** поставщик будет выполнять объект **Command** напрямую, не создавая скомпилную версию.</span><span class="sxs-lookup"><span data-stu-id="123fa-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="123fa-111">Если поставщик не поддерживает подготовку команд, он может возвращать ошибку, как только для этого **свойства** установлено true.</span><span class="sxs-lookup"><span data-stu-id="123fa-111">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**.</span></span> <span data-ttu-id="123fa-112">Если ошибка не возвращается, она просто игнорирует запрос на подготовку команды и задает для свойства **Prepared** свойство **False.**</span><span class="sxs-lookup"><span data-stu-id="123fa-112">If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

