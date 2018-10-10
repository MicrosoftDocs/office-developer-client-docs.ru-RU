---
title: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d9bd24d0aff1134a6af77862fd8f011d4ddff9f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482537"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="529d8-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span><span class="sxs-lookup"><span data-stu-id="529d8-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="529d8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="529d8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="529d8-104">Возвращаемый объект **набора записей** доступна для использования.</span><span class="sxs-lookup"><span data-stu-id="529d8-104">The returned **Recordset** object is available for use.</span></span> <span data-ttu-id="529d8-105">Можно проверить, перейдите или измените его так, как и любой другой **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="529d8-105">You can examine, navigate, or edit it as you would any other **Recordset**.</span></span> <span data-ttu-id="529d8-106">Что можно сделать с помощью **набора записей** зависит от среды.</span><span class="sxs-lookup"><span data-stu-id="529d8-106">What you can do with the **Recordset** depends on your environment.</span></span> <span data-ttu-id="529d8-107">Visual Basic и Visual C++ имеют визуальные элементы управления, которые могут использовать **записей** прямо или косвенно с помощью Включение управления данными.</span><span class="sxs-lookup"><span data-stu-id="529d8-107">Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="529d8-108">Например при отображении веб-страницы в Microsoft Internet Explorer, может потребоваться отображение данных объекта **набора записей** в элементе управления visual.</span><span class="sxs-lookup"><span data-stu-id="529d8-108">For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="529d8-109">Визуальные элементы управления на веб-странице не может получить доступ к объекта **набора записей** напрямую.</span><span class="sxs-lookup"><span data-stu-id="529d8-109">Visual controls on a Web page cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="529d8-110">Тем не менее они могут доступ к объекту **набора записей** с [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="529d8-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="529d8-111">**RDS. DataControl** становится могут использоваться с помощью визуального элемента управления, если свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) имеет значение в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="529d8-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="529d8-112">Элемент управления visual объект должен иметь значение **RDS. параметра **DATASRC** DataControl**и его свойства **DATAFLD** поля объекта **набора записей** (столбца).</span><span class="sxs-lookup"><span data-stu-id="529d8-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="529d8-113">В этом руководстве задайте для свойства **SourceRecordset** :</span><span class="sxs-lookup"><span data-stu-id="529d8-113">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

