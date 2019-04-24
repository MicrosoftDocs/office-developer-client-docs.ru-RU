---
title: Свойство StayInSync (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308493"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="6a4ab-102">Свойство StayInSync (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a4ab-102">StayInSync property (ADO)</span></span>


<span data-ttu-id="6a4ab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a4ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a4ab-104">Указывает, изменяется ли ссылка на базовые дочерние записи (то есть глава) в иерархическом объекте \*\* [Recordset](recordset-object-ado.md) при изменении положения родительской строки.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6a4ab-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6a4ab-105">Settings and return values</span></span>

<span data-ttu-id="6a4ab-106">Задает или возвращает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-106">Sets or returns a **Boolean** value.</span></span> <span data-ttu-id="6a4ab-107">Значение по умолчанию — **True**.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-107">The default value is **True**.</span></span> <span data-ttu-id="6a4ab-108">Если этот параметр **имеет значение true**, глава будет обновлена, если родительский объект **Recordset** изменяет положение строки; Если задано **значение false**, в главе будут содержаться ссылки на данные из предыдущей главы, несмотря на то, что родительский объект **Recordset** изменил положение строки.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-108">If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4ab-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a4ab-109">Remarks</span></span>

<span data-ttu-id="6a4ab-110">Это свойство применяется к иерархическим наборам записей, например, поддерживаемым [службой формирования данных (Майкрософт) для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), и должна быть задана для родительского объекта **Recordset** перед получением дочернего **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6a4ab-110">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved.</span></span> <span data-ttu-id="6a4ab-111">Это свойство упрощает навигацию по иерархическим наборам записей.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-111">This property simplifies navigating hierarchical recordsets.</span></span>

