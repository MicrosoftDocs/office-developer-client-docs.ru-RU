---
title: Свойство Recordset2.ParentRecordset (DAO)
TOCTitle: ParentRecordset Property
ms:assetid: 816cc92e-e530-6ca6-65b0-3165221835a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196492(v=office.15)
ms:contentKeyID: 48545948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101188
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 31f5e0b4dbb924c57c6a94e80cfb98e119292bd7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922491"
---
# <a name="recordset2parentrecordset-property-dao"></a><span data-ttu-id="229cb-102">Свойство Recordset2.ParentRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="229cb-102">Recordset2.ParentRecordset property (DAO)</span></span>


<span data-ttu-id="229cb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="229cb-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="229cb-104">Возвращает родительский **записей** из указанного набора записей.</span><span class="sxs-lookup"><span data-stu-id="229cb-104">Returns the parent **Recordset** of the specified recordset.</span></span> <span data-ttu-id="229cb-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="229cb-105">Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="229cb-106">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="229cb-106">Version Information</span></span>

<span data-ttu-id="229cb-107">Добавлена версия: Access 2007
</span><span class="sxs-lookup"><span data-stu-id="229cb-107">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="229cb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="229cb-108">Syntax</span></span>

<span data-ttu-id="229cb-109">*выражение* . ParentRecordset</span><span class="sxs-lookup"><span data-stu-id="229cb-109">*expression* .ParentRecordset</span></span>

<span data-ttu-id="229cb-110">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="229cb-110">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="229cb-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="229cb-111">Remarks</span></span>

<span data-ttu-id="229cb-112">Свойство **ParentRecordset** возвращает **значение Null** , если указанный набор записей представляет многозначное поле.</span><span class="sxs-lookup"><span data-stu-id="229cb-112">The **ParentRecordset** property returns **Null** if the specifed recordset does not represent a multi-valued field.</span></span>

