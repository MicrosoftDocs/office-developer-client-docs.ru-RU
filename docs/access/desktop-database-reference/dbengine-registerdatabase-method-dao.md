---
title: Метод DBEngine.RegisterDatabase (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715608"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="078f2-102">Метод DBEngine.RegisterDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="078f2-102">DBEngine.RegisterDatabase method (DAO)</span></span>

<span data-ttu-id="078f2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="078f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="078f2-104">Вводит сведения о подключении к источнику данных ODBC в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="078f2-104">Enters connection information for an ODBC data source in the Windows Registry.</span></span> <span data-ttu-id="078f2-105">Драйвер ODBC требуются данные подключения при открытии источника данных во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="078f2-105">The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="078f2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="078f2-106">Syntax</span></span>

<span data-ttu-id="078f2-107">*выражение* . RegisterDatabase (***уведомления о доставке***, ***драйвер***, ***Автоматическая***, ***атрибуты***)</span><span class="sxs-lookup"><span data-stu-id="078f2-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="078f2-108">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="078f2-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="078f2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="078f2-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="078f2-110">Имя</span><span class="sxs-lookup"><span data-stu-id="078f2-110">Name</span></span></p></th>
<th><p><span data-ttu-id="078f2-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="078f2-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="078f2-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="078f2-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="078f2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="078f2-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="078f2-114"><em>Уведомления о доставке</em></span><span class="sxs-lookup"><span data-stu-id="078f2-114"><em>Dsn</em></span></span></p></td>
<td><p><span data-ttu-id="078f2-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="078f2-115">Required</span></span></p></td>
<td><p><span data-ttu-id="078f2-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="078f2-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="078f2-117">имя, используемое в методе <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="078f2-117">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method.</span></span> <span data-ttu-id="078f2-118">Он ссылается на блок описательные сведения об источнике данных.</span><span class="sxs-lookup"><span data-stu-id="078f2-118">It refers to a block of descriptive information about the data source.</span></span> <span data-ttu-id="078f2-119">Например если источник данных ODBC удаленной базы данных, может быть имя сервера.</span><span class="sxs-lookup"><span data-stu-id="078f2-119">For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="078f2-120"><em>Driver</em></span><span class="sxs-lookup"><span data-stu-id="078f2-120"><em>Driver</em></span></span></p></td>
<td><p><span data-ttu-id="078f2-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="078f2-121">Required</span></span></p></td>
<td><p><span data-ttu-id="078f2-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="078f2-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="078f2-123">Имя драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="078f2-123">The name of the ODBC driver.</span></span> <span data-ttu-id="078f2-124">Это не имя DLL-файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="078f2-124">This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="078f2-125"><em>Автоматическая</em></span><span class="sxs-lookup"><span data-stu-id="078f2-125"><em>Silent</em></span></span></p></td>
<td><p><span data-ttu-id="078f2-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="078f2-126">Required</span></span></p></td>
<td><p><span data-ttu-id="078f2-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="078f2-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="078f2-128"><strong>Значение true,</strong> Если вы не хотите отображение диалоговых окон драйвера ODBC, запрашивающие сведения; или <strong>значение False,</strong> Если необходимо отобразить диалоговые окна драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="078f2-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="078f2-129">Если автоматическая имеет <strong>значение True</strong>, атрибуты должно содержать все необходимые сведения или диалоговые окна отображаются все равно.</span><span class="sxs-lookup"><span data-stu-id="078f2-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="078f2-130"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="078f2-130"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="078f2-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="078f2-131">Required</span></span></p></td>
<td><p><span data-ttu-id="078f2-132"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="078f2-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="078f2-133">Список ключевых слов для добавления к реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="078f2-133">A list of keywords to be added to the Windows Registry.</span></span> <span data-ttu-id="078f2-134">Ключевые слова находятся в возврат каретки return – запятой строку.</span><span class="sxs-lookup"><span data-stu-id="078f2-134">The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="078f2-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="078f2-135">Remarks</span></span>

<span data-ttu-id="078f2-136">Если база данных уже зарегистрирована (сведения о подключении к уже введены) в реестре Windows при использовании метода **RegisterDatabase** обновляется сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="078f2-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="078f2-137">В случае сбоя метода **RegisterDatabase** по любой причине никаких изменений не производится реестра Windows, и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="078f2-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="078f2-138">Дополнительные сведения о драйверы ODBC, такие как SQL Server файл справки, входящие в состав драйвера см.</span><span class="sxs-lookup"><span data-stu-id="078f2-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="078f2-139">Пример</span><span class="sxs-lookup"><span data-stu-id="078f2-139">Example</span></span>

<span data-ttu-id="078f2-140">В этом примере используется метод **RegisterDatabase** для регистрации источника данных Microsoft SQL Server с именем издателей в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="078f2-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

