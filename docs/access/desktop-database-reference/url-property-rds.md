---
title: Свойство URL (Справочник по базам данных для рабочих столов RDS)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313400"
---
# <a name="url-property-rds"></a><span data-ttu-id="47b2d-102">Свойство URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="47b2d-102">URL property (RDS)</span></span>

<span data-ttu-id="47b2d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47b2d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47b2d-104">Указывает строку, содержащую относительный или абсолютный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="47b2d-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="47b2d-105">Свойство **URL** можно задать во время конструирования в теге объекта [элемента управления](datacontrol-object-rds.md) DataObject или во время выполнения в коде скрипта.</span><span class="sxs-lookup"><span data-stu-id="47b2d-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b2d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47b2d-106">Syntax</span></span>

<span data-ttu-id="47b2d-107">Время конструирования \<: param Name = "URL" значение = "Server"\></span><span class="sxs-lookup"><span data-stu-id="47b2d-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="47b2d-108">Время выполнения: Control. URL = "Server"</span><span class="sxs-lookup"><span data-stu-id="47b2d-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="47b2d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="47b2d-109">Parameters</span></span>

|<span data-ttu-id="47b2d-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="47b2d-110">Parameter</span></span>|<span data-ttu-id="47b2d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="47b2d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="47b2d-112">*Server*</span><span class="sxs-lookup"><span data-stu-id="47b2d-112">*Server*</span></span> |<span data-ttu-id="47b2d-113">**Строковое** значение, содержащее допустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="47b2d-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="47b2d-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="47b2d-114">*DataControl*</span></span> |<span data-ttu-id="47b2d-115">Объектная переменная, представляющая объект **управления** DataObject.</span><span class="sxs-lookup"><span data-stu-id="47b2d-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="47b2d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="47b2d-116">Remarks</span></span>

<span data-ttu-id="47b2d-117">Как правило, URL-адрес определяет активный файл страницы сервера (ASP), который может создавать и возвращать [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="47b2d-117">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="47b2d-118">Таким образом, пользователь может получить **набор записей** , не выполняя серверный объект [](datafactory-object-rdsserver.md) данных DataObject или запрограммировать настраиваемый бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="47b2d-118">Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="47b2d-119">Если задано свойство **URL** , [SubmitChanges](submitchanges-method-rds.md) отправит изменения в расположении, указанном с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="47b2d-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

