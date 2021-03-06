---
title: ICorDebugILCode2::GetInstrumentedILMap 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILCode2.GetInstrumentedILMap
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 7a4e3085-8f95-40ef-a4be-7d6146f47ce2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a712ed9e3534ca6bb2962989f1ab3750a25d539
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417897"
---
# <a name="icordebugilcode2getinstrumentedilmap-method"></a>ICorDebugILCode2::GetInstrumentedILMap 方法
[仅在 .NET Framework 4.5.2 及更高版本中受支持]  
  
 返回从探查器检测到的中间语言 (IL) 偏移量到此实例的原始方法的 IL 偏移量的映射。  
  
## <a name="syntax"></a>语法  
  
```cpp
HRESULT GetInstrumentedILMap(  
   [in] ULONG32 cMap,  
   [out] ULONG32 *pcMap,  
   [out, size_is(cMap), length_is(*pcMap)] COR_IL_MAP map[]  
);  
```  
  
#### <a name="parameters"></a>参数  
 cMap  
 [in] `map` 数组的存储容量。 有关详细信息，请参阅备注部分。  
  
 pcMap  
 [out]COR_IL_MAP 写入映射数组的值的数目。  
  
 map  
 [out]提供的信息在映射从探查器检测到的 IL 到原始方法的 IL 的 COR_IL_MAP 值的数组。  
  
## <a name="remarks"></a>备注  
 如果探查器通过调用设置映射[icorprofilerinfo:: Setilinstrumentedcodemap](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilinstrumentedcodemap-method.md)方法，则调试器可以调用此方法来检索该映射和内部使用该映射，当计算 IL 偏移量堆栈跟踪和变量生存期。  
  
 如果`cMap`为 0 和`pcMap`为非**null**，`pcMap`设置为可用 COR_IL_MAP 值的数目。 如果 `cMap` 为非零，则它表示 `map` 数组的存储容量。 方法返回时，`map`最多包含`cMap`项，和`pcMap`设置为实际写入的 COR_IL_MAP 值的数目`map`数组。  
  
 如果尚未检测到 IL 或探查器没有提供映射，则此方法将返回 `S_OK` 并将 `pcMap` 设置为 0。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [Icorprofilerinfo:: Setilinstrumentedcodemap](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilinstrumentedcodemap-method.md)  
 [ICorDebugILCode2 接口](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-interface.md)  
 [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
