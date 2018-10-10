---
title: Field2.Expression Property (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f3cbb7ca4078fb92ad721d85679dabee9237f85
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481967"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="0b92b-102">Field2.Expression Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0b92b-102">Field2.Expression Property (DAO)</span></span>

<span data-ttu-id="0b92b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b92b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0b92b-104">Получает или задает выражение, представляющее формулу для вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="0b92b-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="0b92b-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="0b92b-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="0b92b-106">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="0b92b-106">Version Information</span></span>

<span data-ttu-id="0b92b-107">Добавлена версия: Access 2010
</span><span class="sxs-lookup"><span data-stu-id="0b92b-107">Version Added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="0b92b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b92b-108">Syntax</span></span>

<span data-ttu-id="0b92b-109">*выражение* . Выражение</span><span class="sxs-lookup"><span data-stu-id="0b92b-109">*expression* .Expression</span></span>

<span data-ttu-id="0b92b-110">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="0b92b-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b92b-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="0b92b-111">Remarks</span></span>

<span data-ttu-id="0b92b-112">В Access 2013 можно создавать поля в таблице, вычисление значений.</span><span class="sxs-lookup"><span data-stu-id="0b92b-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="0b92b-113">Расчеты могут включать значения из полей в одной таблицы, а также встроенных функций доступа.</span><span class="sxs-lookup"><span data-stu-id="0b92b-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="0b92b-114">Расчет не может содержать поля из таблицы или запросы.</span><span class="sxs-lookup"><span data-stu-id="0b92b-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="0b92b-115">Результаты расчета доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0b92b-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="0b92b-116">Пример</span><span class="sxs-lookup"><span data-stu-id="0b92b-116">Example</span></span>

<span data-ttu-id="0b92b-117">Следующий пример демонстрирует создание вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="0b92b-117">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="0b92b-118">Метод CreateField создает поле с именем **полное имя**.</span><span class="sxs-lookup"><span data-stu-id="0b92b-118">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="0b92b-119">Выражение затем задано значение выражения, вычисляющий значение поля.</span><span class="sxs-lookup"><span data-stu-id="0b92b-119">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="0b92b-120">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0b92b-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

