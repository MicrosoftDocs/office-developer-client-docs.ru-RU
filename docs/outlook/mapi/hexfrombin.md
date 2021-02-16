---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412578"
---
# <a name="hexfrombin"></a><span data-ttu-id="30b3a-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="30b3a-103">HexFromBin</span></span>

  
  
<span data-ttu-id="30b3a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30b3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30b3a-105">Преобразует двоичное число в строку, представленную в hexadecimal number.</span><span class="sxs-lookup"><span data-stu-id="30b3a-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30b3a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="30b3a-106">Header file:</span></span>  <br/> |<span data-ttu-id="30b3a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="30b3a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="30b3a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="30b3a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30b3a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30b3a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30b3a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="30b3a-110">Called by:</span></span>  <br/> |<span data-ttu-id="30b3a-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="30b3a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="30b3a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="30b3a-112">Parameters</span></span>

 <span data-ttu-id="30b3a-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="30b3a-113">_pb_</span></span>
  
> <span data-ttu-id="30b3a-114">[in] Указатель на двоичные данные, которые необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="30b3a-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="30b3a-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="30b3a-115">_cb_</span></span>
  
> <span data-ttu-id="30b3a-116">[in] Размер двоичных данных, на которые указывает параметр PB в _bytes._</span><span class="sxs-lookup"><span data-stu-id="30b3a-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="30b3a-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="30b3a-117">_sz_</span></span>
  
> <span data-ttu-id="30b3a-118">[out] Указатель на строку ASCII с нулью, представляющую двоичные данные в шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="30b3a-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30b3a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30b3a-119">Return value</span></span>

<span data-ttu-id="30b3a-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="30b3a-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30b3a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="30b3a-121">Remarks</span></span>

<span data-ttu-id="30b3a-122">Функция **HexFromBin** принимает указатель на единицу двоичных данных, размер которых указывается параметром _cb._</span><span class="sxs-lookup"><span data-stu-id="30b3a-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="30b3a-123">Он возвращается в строке  _sz_ в пределах (2\*  _cb_)+1 bytes памяти, представление этой двоичной информации в hexadecimal numbers.</span><span class="sxs-lookup"><span data-stu-id="30b3a-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="30b3a-124">Если, например, значением в десятичной части является десятичная 10, то строка будет иметь значение 0A, поэтому один из них преобразуется в два в строке.</span><span class="sxs-lookup"><span data-stu-id="30b3a-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

