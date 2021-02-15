---
title: Свойство DBEngine.DefaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294350"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="4bc7b-102">Свойство DBEngine.DefaultUser (DAO)</span><span class="sxs-lookup"><span data-stu-id="4bc7b-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="4bc7b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bc7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bc7b-104">Задает имя пользователя, используемого для создания рабочей **области по** умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-104">Sets the user name used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="4bc7b-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc7b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bc7b-106">Syntax</span></span>

<span data-ttu-id="4bc7b-107">*выражение .* DefaultUser</span><span class="sxs-lookup"><span data-stu-id="4bc7b-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="4bc7b-108">*выражение*: выражение, возвращающее объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bc7b-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="4bc7b-109">Remarks</span></span>

<span data-ttu-id="4bc7b-110">Параметр **defaultUser —** это строка типа данных.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="4bc7b-111">В рабочей области Microsoft Access это может быть от 1 до 20 символов, в том числе буквы, знаки с акцентами, цифры, пробелы и символы, кроме: " (кавычка), / \\ (косая черта) (косая черта), \[ \] (скобки), : (двоеточие), | (конвейер), \< (знак меньше \> знака), + (знак плюса), = (знак равного знака), ; (точка с запятой), , ( запятая), ?</span><span class="sxs-lookup"><span data-stu-id="4bc7b-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="4bc7b-112">(вопросительный знак), (звездочка), пробелы в окнах и символы управления \* (ОТ ASCII 00 до ASCII 31).</span><span class="sxs-lookup"><span data-stu-id="4bc7b-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="4bc7b-113">Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-113">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="4bc7b-114">В ненадежных паролях не используются сочетания таких элементов.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-114">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="4bc7b-115">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-115">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="4bc7b-116">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-116">Weak password: House27.</span></span> <span data-ttu-id="4bc7b-117">Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-117">Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="4bc7b-118">По умолчанию свойству **DefaultUser** задается значение admin, а свойству **DefaultPassword** — строка нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="4bc7b-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="4bc7b-119">Имена пользователей обычно не чувствительны к делу; Однако при повторном создании учетной записи пользователя, которая была удалена или создана в другой группе, имя пользователя должно точно совпадать с исходным именем с учетом конкретного случая.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-119">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name.</span></span> <span data-ttu-id="4bc7b-120">В паролях учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-120">Passwords are case-sensitive.</span></span>

<span data-ttu-id="4bc7b-121">Как правило, метод **CreateWorkspace** используется для создания объекта **Workspace** с заданным именем пользователя и паролем.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-121">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password.</span></span> <span data-ttu-id="4bc7b-122">Однако для обеспечения обратной совместимости с более ранними версиями и для удобства, когда не реализована защищенная база данных, ядр базы данных Microsoft Access автоматически создает объект **Рабочей** области по умолчанию, если он еще не открыт.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-122">However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open.</span></span> <span data-ttu-id="4bc7b-123">В этом случае значения свойств **DefaultUser** и **DefaultPassword** определяют пользователя и пароль для объекта **рабочей** области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-123">In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="4bc7b-124">Чтобы это свойство вступает в силу, необходимо установить его перед вызовом любых методов DAO.</span><span class="sxs-lookup"><span data-stu-id="4bc7b-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

