---
title: Свойство Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292071"
---
# <a name="handler-property-rds"></a><span data-ttu-id="eaadc-102">Свойство Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="eaadc-102">Handler property (RDS)</span></span>

<span data-ttu-id="eaadc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eaadc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eaadc-104">Указывает имя программы настройки на стороне сервера (обработчика), которая расширяет [функциональность RDSServer.DataFactory](datafactory-object-rdsserver.md)и любые параметры, используемые обработчиком. </span><span class="sxs-lookup"><span data-stu-id="eaadc-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaadc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eaadc-105">Syntax</span></span>

<span data-ttu-id="eaadc-106">*DataControl*. Обработник = *String*</span><span class="sxs-lookup"><span data-stu-id="eaadc-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="eaadc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaadc-107">Parameters</span></span>

|<span data-ttu-id="eaadc-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="eaadc-108">Parameter</span></span>|<span data-ttu-id="eaadc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="eaadc-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="eaadc-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="eaadc-110">*DataControl*</span></span> |<span data-ttu-id="eaadc-111">Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="eaadc-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="eaadc-112">*String*</span><span class="sxs-lookup"><span data-stu-id="eaadc-112">*String*</span></span> |<span data-ttu-id="eaadc-113">**Строковое** значение, содержаее имя обработера и любые параметры, разделенные запятой (например, "handlerName,parm1,parm2,...,parm *N"*).</span><span class="sxs-lookup"><span data-stu-id="eaadc-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="eaadc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="eaadc-114">Remarks</span></span>

<span data-ttu-id="eaadc-115">Это свойство поддерживает настройку, которая требует настройки свойства [CursorLocation](cursorlocation-property-ado.md) **в adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="eaadc-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="eaadc-116">Имя обработера и его параметры, если таковые имеются, разделены запятой (",").</span><span class="sxs-lookup"><span data-stu-id="eaadc-116">The name of the handler and its parameters, if any, are separated by commas (",").</span></span> <span data-ttu-id="eaadc-117">Непредсказуемое поведение приведет, если в строке появится полуколон (";"). </span><span class="sxs-lookup"><span data-stu-id="eaadc-117">Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*.</span></span> <span data-ttu-id="eaadc-118">Вы можете написать собственный обработчик, если он поддерживает **интерфейс IDataFactoryHandler.**</span><span class="sxs-lookup"><span data-stu-id="eaadc-118">You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="eaadc-119">Имя обработера по умолчанию **— MSDFMAP. Обработник** и его параметр по умолчанию — это файл настройки с **именемMSDFMAP.INI**.</span><span class="sxs-lookup"><span data-stu-id="eaadc-119">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**.</span></span> <span data-ttu-id="eaadc-120">Используйте это свойство для вызова альтернативных файлов настройки, созданных администратором сервера.</span><span class="sxs-lookup"><span data-stu-id="eaadc-120">Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="eaadc-121">Альтернатива настройке свойства **Обработка** — указать обработник и параметры в [свойстве ConnectionString;](connectionstring-property-ado.md) то есть "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="eaadc-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

