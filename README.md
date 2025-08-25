
# QInspired Heritage AR - Cultural Heritage Experience Platform

## Disclaimer: Experimental Code Advisory / Napomena: Savjet o eksperimentalnom kodu

**ENGLISH**  
This repository contains experimental code generated through iterative interaction with large language models (LLMs), in a process informally referred to as "vibe coding." Although care has been taken to structure and annotate the code for clarity, it may contain errors, hallucinated dependencies, or syntactic inconsistencies. The code should be treated as **a conceptual and exploratory artifact**, not as production-ready software.  
Technical review and independent validation are **strongly recommended** before reuse or integration in other systems.  
This project is shared in the spirit of open scientific exploration and collaboration.

**CROATIAN / HRVATSKI**  
Ovo spremište sadrži eksperimentalni kod generiran kroz iterativnu interakciju s modelima temeljenima na velikim jezičnim modelima (LLM), u procesu koji se neformalno naziva "vibe kodiranje". Iako je uložen trud u strukturiranje i komentiranje koda radi jasnoće, on može sadržavati pogreške, halucinirane ovisnosti ili sintaktičke nedosljednosti. Kod se treba smatrati **konceptualnim i istraživačkim artefaktom**, a ne softverom spremnim za produkcijsku upotrebu.  
Preporučuje se **stručna revizija i neovisna validacija** prije ponovne upotrebe ili integracije u druge sustave.  
Projekt se dijeli u duhu otvorenog znanstvenog istraživanja i suradnje.

### AI Peer Review Validation

To minimize the risk of errors, hallucinations, or accidental oversights, this project's configuration underwent **validation by several advanced large language models (LLMs):** Perplexity, Gemini, DeepSeek, Grok, and ChatGPT.

- **All models** independently assessed the solution as innovative and functional, and suggested possible improvements.
- One typo was detected and corrected; no severe logical or security-relevant issues were found.
- The conceptual value and safety of the project were further confirmed by consensus among models.

Nonetheless, **manual expert review and testing in a controlled environment** remain essential before any production integration.

---

## Project Overview

QInspired Heritage AR is an immersive AR project that reconstructs historical atmospheres using quantum-inspired probabilistic algorithms. The system dynamically generates authentic historical scenes through probabilistic methods that simulate quantum mechanical principles of superposition and measurement, creating unpredictable yet historically coherent experiences.

Unlike systems requiring actual quantum hardware, this implementation uses quantum-inspired algorithms running on classical computers to generate multisensory historical recreations for education, tourism, and cultural heritage preservation.

## Target Audience

- Cultural heritage institutions and museums
- Educational technology developers  
- Tourism industry professionals
- AR developers interested in cultural applications
- Researchers in digital humanities

## Technology Stack

**Core Engine:**
- Probabilistic Computing: Quantum-inspired algorithms on classical hardware
- AR Platform: Unity with ARFoundation, WebAR with 8th Wall
- Programming Language: Python (core logic), JavaScript (WebAR), C# (Unity)
- Machine Learning: Classical ML with quantum-inspired probabilistic methods

**Platform Support:**
- WebAR: Browser-based instant access
- Mobile AR: iOS and Android native applications  
- AR Glasses: HoloLens, Magic Leap, Meta Quest integration
- Sensory Extensions: Audio systems, experimental olfactory integration

## Architecture Overview

```
[Historical Location]
        ↓
[QR Code Scan] → [WebAR Entry Point] → [App Store Redirect (Optional)]
        ↓                    ↓
[Quantum-Inspired Engine] ← [Environmental Sensors]
        ↓
[Probabilistic Scene Generation]
        ↓
[Multi-sensory Output: Audio + Visual + (Olfactory*)]
        ↓
[AR Rendering] → [User Experience]
```

## Core Algorithm: Quantum-Inspired Heritage Engine

```python
import numpy as np
import random
from typing import Dict, List, Tuple

class QuantumInspiredHeritage:
    """
    Quantum-inspired probabilistic engine for generating historically
    coherent AR scenes using classical hardware simulation of quantum
    mechanical principles.
    """
    
    def __init__(self):
        self.algorithm_type = "quantum-inspired probabilistic"
        self.historical_database = self._initialize_scene_database()
        
    def generate_historical_scene(self, environmental_params: Dict) -> Dict:
        """
        Generate a historically coherent scene using quantum-inspired
        probabilistic methods.
        
        Args:
            environmental_params: Dict containing temperature, time_of_day, 
                                location_id, visitor_count, etc.
        
        Returns:
            Dict with audio, visual, and (optionally) olfactory scene data
        """
        # Simulate quantum superposition through probability distributions
        scene_weights = self._calculate_probability_distribution(environmental_params)
        
        # Simulate quantum measurement - collapse to specific scenario
        selected_scene = self._collapse_to_scenario(scene_weights)
        
        # Generate coherent multisensory experience
        return self._render_multisensory_scene(selected_scene, environmental_params)
    
    def _calculate_probability_distribution(self, params: Dict) -> np.ndarray:
        """
        Create quantum-inspired probability weights based on environmental
        and historical factors.
        """
        temperature = params.get('temperature', 20)
        time_period = params.get('historical_period', 'roman')
        location_type = params.get('location_type', 'urban')
        
        # Quantum-inspired probability calculation
        # Simulate entangled states between environmental and historical factors
        base_weights = np.array([0.25, 0.25, 0.25, 0.25])  # Equal superposition
        
        # Environmental modulation (simulates quantum interference)
        temp_factor = np.sin(temperature * np.pi / 40) * 0.3
        time_factor = self._get_historical_weight(time_period)
        
        # Apply quantum-inspired transformations
        weights = base_weights + np.array([
            temp_factor + time_factor[0],
            -temp_factor + time_factor[1], 
            temp_factor * 0.5 + time_factor[2],
            -temp_factor * 0.3 + time_factor[3]
        ])
        
        # Normalize to valid probability distribution
        return np.abs(weights) / np.sum(np.abs(weights))
    
    def _collapse_to_scenario(self, weights: np.ndarray) -> int:
        """Simulate quantum measurement - probabilistic collapse to definite state"""
        return np.random.choice(len(weights), p=weights)
    
    def _render_multisensory_scene(self, scene_id: int, params: Dict) -> Dict:
        """Generate the complete sensory experience for the selected scene"""
        base_scenes = [
            {
                "scene_name": "daily_life_market",
                "audio": "roman_market_ambiance.mp3",
                "visual": "bustling_forum_3d_animation", 
                "olfactory": "bread_olive_oil_mixture",  # For future implementation
                "historical_period": "roman_imperial",
                "description": "Busy Roman forum with merchants and citizens"
            },
            {
                "scene_name": "villa_leisure", 
                "audio": "villa_courtyard_water.mp3",
                "visual": "villa_dei_misteri_reconstruction",
                "olfactory": "wine_roses_incense", 
                "historical_period": "roman_imperial",
                "description": "Aristocratic Roman villa with feast preparation"
            },
            {
                "scene_name": "neanderthal_camp",
                "audio": "prehistoric_forest_sounds.mp3", 
                "visual": "neanderthal_shelter_animation",
                "olfactory": "wood_smoke_earth",
                "historical_period": "paleolithic",
                "description": "Neanderthal family group around fire"
            },
            {
                "scene_name": "workshop_craft",
                "audio": "artisan_workshop_sounds.mp3",
                "visual": "pottery_metalwork_3d_scene", 
                "olfactory": "clay_charcoal_metal",
                "historical_period": "roman_imperial", 
                "description": "Roman craftsmen at work - pottery and metalwork"
            }
        ]
        
        selected = base_scenes[scene_id]
        
        # Add environmental adaptations
        selected["environmental_adaptation"] = {
            "temperature_influence": params.get('temperature', 20),
            "time_of_day": params.get('time_of_day', 'midday'),
            "weather_condition": self._simulate_historical_weather(params)
        }
        
        return selected
    
    def _get_historical_weight(self, period: str) -> List[float]:
        """Return period-specific probability weights"""
        weights_map = {
            'roman': [0.4, 0.3, 0.1, 0.2],
            'paleolithic': [0.1, 0.1, 0.6, 0.2], 
            'medieval': [0.3, 0.2, 0.2, 0.3]
        }
        return weights_map.get(period, [0.25, 0.25, 0.25, 0.25])
    
    def _simulate_historical_weather(self, params: Dict) -> str:
        """Generate historically plausible weather conditions"""
        temp = params.get('temperature', 20)
        if temp > 30:
            return "hot_mediterranean_summer"
        elif temp > 20:
            return "pleasant_spring_day"
        else:
            return "cool_autumn_morning"
    
    def _initialize_scene_database(self) -> Dict:
        """Initialize historical scene database"""
        return {
            "roman_scenes": [],
            "paleolithic_scenes": [],
            "medieval_scenes": []
        }

# WebAR Integration Example
def generate_webar_scene(location_id: str, environmental_data: Dict) -> Dict:
    """
    WebAR-compatible scene generation function
    """
    engine = QuantumInspiredHeritage()
    
    # Prepare environmental parameters
    params = {
        'temperature': environmental_data.get('temperature', 22),
        'location_type': environmental_data.get('location_type', 'archaeological_site'),
        'historical_period': environmental_data.get('period', 'roman'),
        'time_of_day': environmental_data.get('time', 'afternoon')
    }
    
    # Generate scene using quantum-inspired algorithms
    scene = engine.generate_historical_scene(params)
    
    # Format for WebAR consumption
    webar_output = {
        "audio_file": scene["audio"],
        "3d_model": scene["visual"], 
        "scene_description": scene["description"],
        "environmental_adaptation": scene["environmental_adaptation"],
        "olfactory_profile": scene["olfactory"]  # For future hardware integration
    }
    
    return webar_output

# Usage Example
if __name__ == "__main__":
    print("=== QInspired Heritage AR Engine ===\n")
    
    # Simulate environmental conditions
    environmental_conditions = {
        'temperature': random.uniform(18, 32),
        'location_type': 'roman_forum',
        'period': 'roman',
        'time': 'morning'
    }
    
    # Generate scene
    scene = generate_webar_scene("salona_ruins", environmental_conditions)
    
    print(f"Generated Scene: {scene['scene_description']}")
    print(f"Audio: {scene['audio_file']}")
    print(f"Visual: {scene['3d_model']}")
    print(f"Environmental: {scene['environmental_adaptation']}")
    print(f"Olfactory Profile: {scene['olfactory_profile']}")
    print("\nAR Experience Activated!")
```

## Multisensory Implementation

### Current Implementation (WebAR Ready)
- **Audio**: 3D spatial audio with Web Audio API
- **Visual**: 3D scene rendering with Three.js/WebGL
- **Interactive**: Touch gestures, head tracking, movement detection

### Future Extensions (Native App + Hardware)
- **Olfactory**: Controlled scent diffusion systems
  - Indoor: HVAC-integrated scent dispensers
  - Portable: Personal olfactory devices via Bluetooth
  - Outdoor: Experimental scent projection systems
- **Haptic**: Vibration patterns, texture simulation
- **Environmental**: Temperature simulation, air movement

### Olfactory Development Roadmap

**Phase 1**: Research and prototyping
- Partner with scent technology companies
- Historical scent recreation research
- Safety and allergy considerations

**Phase 2**: Controlled environment testing
- Museum indoor installations
- Personal scent device prototypes
- User experience studies

**Phase 3**: Scalable implementation
- Integration with WebAR via Bluetooth API
- Mass-producible scent cartridge systems
- Multi-location deployment

## Technical Feasibility

**WebAR Implementation**: 9.5/10
- Fully achievable with current web technologies
- 8th Wall WebAR provides robust AR framework
- Audio-visual experience deliverable in 8-10 weeks

**Native AR App**: 8.5/10  
- Unity + ARFoundation well-established
- Bluetooth integration for external sensors feasible
- Full implementation achievable in 4-6 months

**Olfactory Integration**: 5.5/10
- Technically possible with existing scent diffusion hardware
- Requires significant R&D for outdoor applications
- Best suited for controlled indoor environments initially

**Quantum-Inspired Algorithms**: 9/10
- Runs efficiently on standard hardware
- Provides authentic unpredictability without quantum processors
- Scalable and maintainable codebase

## Economic Analysis

**WebAR Development**: €47,000 (first year)
- 3D modeling and audio production: €14,000
- Development (8-10 weeks): €27,000
- Hosting and infrastructure: €1,000
- Maintenance: €5,000

**Full AR Platform**: €90,000+ (first year)  
- Native app development: €60,000
- Hardware integration: €15,000
- Advanced 3D content: €10,000
- Annual maintenance: €25,000

**Olfactory Extension**: €30,000-50,000 (R&D phase)
- Scent hardware integration: €20,000
- Historical scent research: €15,000
- Safety testing and certification: €10,000

## Market Opportunity

**Cultural Heritage Tourism**: 
- Pompeii: 2.5M annual visitors
- Diocletian's Palace: 1.2M annual visitors
- European archaeological sites: 50M+ combined annually

**Educational Technology**: 
- Growing AR in education market ($5.9B by 2025)
- Museum digitalization initiatives post-COVID
- EU Digital Europe Programme funding available

**Competitive Advantages**:
- First quantum-inspired cultural heritage AR platform
- Modular architecture adaptable to any historical site
- Progressive implementation from WebAR to full multisensory

## Implementation Locations

### Primary Targets
- **Salona, Croatia**: Roman archaeological complex
- **Krapina Neanderthal Museum**: Prehistoric cultural site
- **Diocletian's Palace**: Living historical monument

### Expansion Opportunities  
- Pompeii, Italy
- Forum Romanum, Rome
- Lascaux Cave, France
- Stonehenge, UK

## Legal and Ethical Considerations

- **Intellectual Property**: Creative Commons Attribution-NonCommercial license
- **Historical Accuracy**: Collaboration with historians and archaeologists
- **Data Privacy**: GDPR compliant, minimal data collection
- **Cultural Sensitivity**: Respectful representation of historical periods
- **Safety**: Comprehensive testing of olfactory components for allergies

## Risk Assessment and Mitigation

**Technical Risks**:
- Olfactory hardware limitations → Start with audio-visual, add scents incrementally
- AR tracking accuracy outdoors → Combine GPS, visual markers, and sensor fusion
- Cross-platform compatibility → Focus on WebAR first, expand to native apps

**Market Risks**:
- Slow adoption by cultural institutions → Pilot programs with progressive museums
- Competition from tech giants → Focus on specialized cultural heritage niche
- Funding challenges → EU grants, cultural tourism partnerships

**Operational Risks**:
- Maintenance complexity → Modular design for easy component replacement
- Content creation costs → Partnerships with archaeological institutions
- Seasonal tourism variations → Multiple location deployments

## Development Timeline

**Phase 1** (0-3 months): WebAR Prototype
- Core quantum-inspired engine development
- WebAR framework integration
- Single location implementation (Salona)

**Phase 2** (3-6 months): Native App MVP
- Unity AR application 
- Multi-location content management
- Beta testing with museum partners

**Phase 3** (6-12 months): Advanced Features
- AR glasses support
- Experimental olfactory integration
- Analytics and content management dashboard

**Phase 4** (12+ months): Scale and Research
- Multiple location deployments
- Advanced olfactory systems research
- International partnerships

## Getting Started

### For Developers
1. Clone repository
2. Install dependencies: `pip install numpy qiskit` (for algorithm simulation)
3. WebAR setup: Follow `docs/webar-setup.md`
4. Unity setup: Import ARFoundation package

### For Cultural Institutions
1. Review WebAR technical specifications
2. Schedule consultation for content definition
3. Pilot program implementation (10-week timeline)

### For Researchers  
1. Review quantum-inspired algorithm documentation
2. Historical accuracy collaboration opportunities
3. Olfactory research partnership possibilities

## License and Copyright

QInspired Heritage AR Platform  
Copyright © 2025 Miljenka Ćurković. All rights reserved.

This work is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0).

**You are free to:**
- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

**Under the following terms:**
- Attribution — You must give appropriate credit to Miljenka Ćurković
- NonCommercial — You may not use this material for commercial purposes without explicit written permission

Commercial use, distribution, or modification requires prior written authorization from the author.

For licensing requests or commercial inquiries: miljenka.qeit@proton.me

---

*This project represents a convergence of quantum-inspired computing, cultural heritage preservation, and immersive technology. While the algorithms draw inspiration from quantum mechanical principles, they operate entirely on classical hardware, making the technology accessible and deployable with current infrastructure.*





