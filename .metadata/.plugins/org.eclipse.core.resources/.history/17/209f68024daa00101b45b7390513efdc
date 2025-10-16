package com.exam.in.service;

import com.exam.in.model.*;
import com.exam.in.repository.*;
import org.springframework.stereotype.Service;

import java.util.List;
import java.util.Optional;

@Service
public class FitnessService {

    private final FitnessRepository repository;

    public FitnessService(FitnessRepository repository) {
        this.repository = repository;
    }

    public Fitness saveFitness(Fitness fitness) {
        return repository.save(fitness);
    }

    public List<Fitness> getAllFitness() {
        return repository.findAll();
    }

    public Optional<Fitness> getFitnessById(Long id) {
        return repository.findById(id);
    }

    public Fitness updateFitness(Long id, Fitness fitnessDetails) {
        Fitness fitness = repository.findById(id).orElseThrow(() -> new RuntimeException("Fitness not found"));
        fitness.setName(fitnessDetails.getName());
        fitness.setAge(fitnessDetails.getAge());
        fitness.setHeight(fitnessDetails.getHeight());
        fitness.setWeight(fitnessDetails.getWeight());
        return repository.save(fitness);
    }

    public void deleteFitness(Long id) {
        repository.deleteById(id);
    }
}
