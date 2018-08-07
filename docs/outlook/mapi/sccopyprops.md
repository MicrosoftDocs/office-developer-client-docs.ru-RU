---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812191"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Относится к**: Outlook 
  
Копирование свойств, определенных в массив структур [SPropValue](spropvalue.md) в новое место назначения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Параметры

 _cprop_
  
> [in] Число свойств для копирования. 
    
 _rgprop_
  
> [in] Указатель на массив структур [SPropValue](spropvalue.md) , которые определяют свойства, которые нужно скопировать. Параметр _rgprop_ не нужно точки в начало массива, но он должен указывать в начало структур **SPropValue** в массиве. 
    
 _pvDst_
  
> [in] Указатель на начальное положение в памяти, к которому эта функция копирует свойства. 
    
 _печатной_
  
> [out] Необязательный указатель на размер, в байтах, блока памяти, на который указывает параметр _pvDst_ . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Свойства были успешно скопированы.
    
MAPI_E_INVALID_PARAMETER
  
> Обнаружен неизвестный тип свойства.
    
## <a name="remarks"></a>Замечания

Новый массив и все данные размещаются в буфера, созданных с помощью одного выделения и функцию [ScRelocProps](screlocprops.md) можно использовать для настройки указателей в отдельных структур [SPropValue](spropvalue.md) . Перед этой настройкой указатели являются допустимыми. 
  
 **ScCopyProps** сохраняет исходный порядок свойств для массива скопированные свойства. 
  
Параметр _печатной_ является необязательным; Если не равно NULL, перейдут в число байтов, сохраненных в параметре _pvDst_ . 
  
## <a name="see-also"></a>См. также



[ScDupPropset](scduppropset.md)

